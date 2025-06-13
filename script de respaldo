#!/bin/bash

# === VARIABLES ===
FECHA=$(date +%F)
BACKUP_DIR="/home/ubuntu/respaldo"
ARCHIVO="respaldo_$FECHA.tar.gz"
ORIGEN="/etc"  # Cambia si quieres respaldar otra carpeta
REMOTE="gdrive:Respaldos"

# === ASEGURARSE DE QUE EL SCRIPT CORRE COMO ROOT ===
if [ "$EUID" -ne 0 ]; then
  echo "❌ Este script debe ejecutarse como root (usa sudo)."
  exit 1
fi

# === CREAR LA CARPETA DE RESPALDOS SI NO EXISTE ===
mkdir -p "$BACKUP_DIR"

# === COMPRIMIR LA CARPETA ===
echo "🔄 Comprimiendo $ORIGEN..."
tar -czf "$BACKUP_DIR/$ARCHIVO" "$ORIGEN" 2> /tmp/respaldo_errores.log

# === SUBIR A GOOGLE DRIVE ===
echo "☁️ Subiendo a Google Drive..."
rclone --config=/home/ubuntu/.config/rclone/rclone.conf copy "$BACKUP_DIR/$ARCHIVO" "$REMOTE"


# === BORRAR RESPALDOS LOCALES ANTIGUOS (mayores a 7 días) ===
echo "🧹 Limpiando respaldos antiguos..."
find "$BACKUP_DIR" -type f -name "*.tar.gz" -mtime +7 -exec rm {} \;

echo "✅ Respaldo completado: $ARCHIVO"
