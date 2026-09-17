# Laboratorio 02 - xv6

Comandos de la Parte A ejecutados en xv6:
![Parte A - Captura 1](imgs/parteA_1.png)
![Parte A - Captura 2](imgs/parteA_2.png)
![Parte A - Captura 3](imgs/parteA_3.png)

## Parte C: Análisis de llamadas al sistema

Se utilizó `grep` para localizar las llamadas al sistema en el código fuente del kernel:

- **fork:** Interfaz `SYS_fork` en `kernel/syscall.h`, implementación `sys_fork` en `kernel/sysproc.c`
- **read:** Interfaz `SYS_read` en `kernel/syscall.h`, implementación `sys_read` en `kernel/sysfile.c`

![Resultado de grep sobre fork y read](imgs/parteC.png)

### Respuesta a la pregunta de reflexión:
La interfaz (`SYS_read`) es solo un identificador entero usado por el proceso en espacio de usuario, mientras que la implementación (`sys_read`) ejecuta la lógica real en modo kernel.
