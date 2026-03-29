# Base de Datos - Zentry

## Modelo principal

### users
- id
- email
- password
- enabled

### roles
- id
- name

### permissions
- id
- name

## Relaciones

- user_roles
- role_permissions

## Enfoque

- Control de acceso basado en roles (RBAC)
- Integridad de datos
- Preparado para multiempresa
