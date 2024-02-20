# Taller Expresiones Regulares

##### **Ejercicio 1: Verificar el Nit**

**Enunciado:** Construya una expresión regular que permita validar en Nit de una empresa en Colombia.

`const  pattern = /^\d{1,2}\.\d{3}\.\d{3}-\d{1}$/;`

`let nit = '12.345.678-9';`

`if (pattern.test(nit)) {`

  `console.log("El nit es válido.");`

`} else {`

  `console.log("El nit no es válido.");`

`}`




##### ** Ejercicio 2: Verificar un código postal**

**Enunciado:** Crea una expresión regular que valide un código postal con el formato de cinco dígitos.

`const postal = /^\d{5}$/;`

`const codigoPostal = "12345";`

`if (postal.test(codigoPostal)) {`

  `console.log("El código postal es válido.");`

`} else {`

  `console.log("El código postal no es válido.");`

`}`



##### **Ejercicio 3: Verificar un formato de correo electrónico**

**Enunciado:** Crea una expresión regular que valide un formato básico de dirección de correo electrónico.

`let include = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;`

`let correo = "jac18@gmail.com";`

`if (include.test(correo)) {`

  `console.log(correo + " es un correo electrónico válido.");`

`} else {`

  `console.log(correo + " no es un correo electrónico válido.");`

`}`



##### **Ejercicio 4: Verificar un número de teléfono**

**Enunciado:** Crea una expresión regular que valide un número de teléfono con el formato (XXX) XXX-XXXX.

`const phone = /^\(\d{3}\) \d{3}-\d{4}$/;`

`const phoneNumber = '(123) 456-7890';`

`if (phone.test(phoneNumber)) {`

  `console.log('El número de teléfono es válido.');`

`} else {`

  `console.log('El número de teléfono no es válido.');`

`}`



**Ejercicio 5: Verificar una dirección URL**

**Enunciado:** Crea una expresión regular que valide una dirección URL básica.

`let patron = /^https?:\/\/.*/;`

`let url = "https://www.google.com/?hl=es";`



`if (patron.test(url)) {`

  `console.log("La URL es válida.");`

`} else {`

  `console.log("La URL no es válida.");`

`}`



##### ** Ejercicio 6: Validar un nombre de usuario**

**Enunciado:** Crea una expresión regular que valide un nombre de usuario. El nombre de usuario debe contener solo letras minúsculas y números, con longitud entre 3 y 10 caracteres.

`let cosas = /^[a-z0-9]{3,10}$/;`

`const nombreUsuario = "usuario123";`

`if (patron.test(nombreUsuario)) {`

  `console.log(El nombre de usuario '${nombreUsuario}' es válido.);`

`} else {`

  `console.log(El nombre de usuario '${nombreUsuario}' no es válido.);`

`}`





##### **Ejercicio 7: Validar una dirección IP**

**Enunciado:** Crea una expresión regular que valide una dirección IP en formato IPv4.



`let IPv4 = /^(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$/;`

`var ipAddress = '192.168.0.1';`

`if (IPv4.test(ipAddress)) {`

  `console.log('La dirección IP es válida.');`

`} else {`

  `console.log('La dirección IP no es válida.');`

`}`



**Ejercicio 8: Validar un formato de fecha**

** Enunciado:** Crea una expresión regular que valide una fecha en formato "dd/mm/yyyy".



`let formato = /^(0[1-9]|[1-2][0-9]|3[0-1])\/(0[1-9]|1[0-2])\/\d{4}$/;`

`let fecha = "31/12/2024";`

`if (formato.test(fecha)) {`

  `console.log("La fecha es válida.");`

`} else {`

  `console.log("La fecha es inválida.");`

`}`



##### **Ejercicio 9: Validar una contraseña segura**

**Enunciado:** Crea una expresión regular que valide una contraseña que cumpla con los siguientes criterios:

- Al menos 8 caracteres de longitud.

- Al menos una letra mayúscula.

- Al menos una letra minúscula.

- Al menos un número.

- Puede contener caracteres especiales como !@#$%^&*()_+.

  

`let validar = /^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[!@#$%^&*()_+.])[A-Za-z\d!@#$%^&*()_+.]{8,}$/;`

`let password = "Abc123!@#";`

`if (validar.test(password)) {`

  `console.log("La contraseña es válida.");`

`} else {`

  `console.log("La contraseña es inválida.");`

`}`