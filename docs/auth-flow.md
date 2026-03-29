# Flujo de Autenticación

## Login

1. Usuario ingresa credenciales
2. Backend valida
3. Se genera JWT
4. Se devuelve al cliente

## Uso del token

Cada request incluye:

Authorization: Bearer TOKEN

## Tipos de acceso

### Público
- No requiere token

### Privado
- Requiere JWT

## Seguridad

- Contraseñas encriptadas
- Tokens con expiración
