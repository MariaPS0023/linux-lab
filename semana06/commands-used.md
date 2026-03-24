#=== Estado final ===
log "INFO" "=== Verificación completada ==="
case "$estado_global" in
	OK)
		log "OK"	"RESULTADO: todos los checks pasaron correctamente."
		exit 0
		;;
	WARNING)
		log "WARNING" "RESULTADO: verificación completada con advertencias."
		exit 0
		;;
	ERROR)
		log "ERROR" "RESULTADO: se detectaron errores que requieren atención."
		exit 1
		;;
esac
