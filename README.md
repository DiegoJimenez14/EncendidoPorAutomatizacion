# Encendido Por Automatizacion
Encendido por automatización inductiva AWS
El siguiente proyecto es parte de la formacion autodicata
Las tablas cuenta con referencia de ensayos y son propeidad de AWS Architected Center 


Autores de solucion 
Febrero de 2023
Travis Cox, Automatización inductiva
Vinod Shukla, Equipo de integración y automatización de AWS

## Contenido de la solución 
- Alta disponibilidad ( 2 AZ)
- VPC 
- 2 Subredes publicas --- Puerta de enlace NAT - Acecso saliente para SB Privadas -- Servidor ignition principal y secundario en las AZ ** Carcteristcas opcionales
- 2 Subredes Privadas --- Cluster de base de datos Aura + Grupo de seguridad: Instancia de base de datos principal que admita operaciones de escritura, 2 instancias de bases de datos de r
  replica que admiten operaciones de lectura
- AWS KMS -- Para el cifrado en reposo para el cluster de base de datos de Aurora
- Amazon CloudWatch para alarma de uso de CPU del host bastion 
- Amazon Simple Notification Service (Amazon SNS) para enviar notificaciones cuando se invoca la alarma de CloudWatch.
## La opción de clúster implementa un par redundante de servidores backend (I/O) de Ignition y dos servidores frontend
detrás de un equilibrador de carga. La implementación de esta solución de 
socios con parámetros predeterminados crea el siguiente entorno de Ignition en la nube de AWS. 

Antes de implementar: leer terminos de licencia 


Procedimeinto independeinte  
 
 Cuenta personal Diego Jiemenez by UserIAM 
 
 Opcion de implementacion 1  -- Ser Único 
 -
  -
   -
    - Crea un entorno de AWS que incluye: VPV, Subredes, puertas de anlace NAT, grupos de segurida, host bastion ** Componentes de arquitectura 
    
 Stack 
 Esta se enciuentra preconfigurada
 
La pila tiene una configuracion de AZ us-east-1 Norte de virginia. De uso habitual personal - 


Pasos previos 
- Leer acuerdos de licencia 
- ingrese 0.0.0.0/0 para el parametro Web access CIDR( WebAccessCIDR) Permite que la implementacion este disponible para internet publico
  tambien puede ingresar bloque CIDR y eliminar el acceso di Ignition a un grupo especifico de IP
  - Tendrá que ingresar sus propios nombres de dominio para la opcion de implementacion de clusters y luego usarlos en el balanceador de carga
  - Los nombres de denominio que se han proporcionado generan un certificado SSL y enciara un correo electronico al administrador de dominio y así
    verificar la propeidad 
  - Luego de la implementacion configure un registro DNS CNAME para el nombre de dominio Ignition.
## Pasos 
Asigrnar nombre: Encendido-Automatización-Inductiva
## Parametros: 
- Network Configuration : Key name - 
- Zonas de disponibilidad
- Acceso web CIDR: 0.0.0.0/0
- Rango de IP permitido - Bloque CIDR para permitir el acceso SSH externo.
- Configuración del bastión de Linux: Crear Pila de bastion: seleccione FALSO sí: no desea implementar la pila de host bastión opcional.
- Configuración de la base de datos: AuroraPostgresDB
- Período de retención de la copia de seguridad de la base de datos: *defecto*
- 
 
      
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    

