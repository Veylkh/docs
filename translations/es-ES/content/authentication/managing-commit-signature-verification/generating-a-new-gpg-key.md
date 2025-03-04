---
title: Generar una llave GPG nueva
intro: 'Si no tienes una llave GPG existentes, puedes generar una nueva llave GPG para usarla para firmar confirmaciones y etiquetas.'
redirect_from:
  - /articles/generating-a-new-gpg-key
  - /github/authenticating-to-github/generating-a-new-gpg-key
  - /github/authenticating-to-github/managing-commit-signature-verification/generating-a-new-gpg-key
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Identity
  - Access management
---

{% data reusables.gpg.supported-gpg-key-algorithms %}

## Generar una llave GPG

{% note %}

**Nota:** Antes de generar una nueva llave GPG, asegúrate de haber verificado tu dirección de correo electrónico. Si no has verificado tu dirección de correo electrónico, no podrás firmar confirmaciones y etiquetas con GPG.{% ifversion fpt or ghec %}Para obtener más información, consulta "[Verificar tu dirección de correo electrónico](/articles/verifying-your-email-address)".{% endif %}

{% endnote %}

1. Descarga e instala [las herramientas de la línea de comando GPG](https://www.gnupg.org/download/) para tu sistema operativo. Generalmente recomendamos instalar la versión más reciente para tu sistema operativo.
{% data reusables.command_line.open_the_multi_os_terminal %}
3. Genera un par de la llave GPG. Ya que existen varias versiones de GPG, puede que necesites consultar la [_página man_](https://en.wikipedia.org/wiki/Man_page) relevante para encontrar el comando adecuado para la generación de llaves. Tu llave debe utilizar RSA.
    - Si estás usando una versión 2.1.17 o superior, copia el siguiente texto para generar un par de la llave GPG.
      ```shell{:copy}
      $ gpg --full-generate-key
      ```
    - Si no estás usando la versión 2.1.17 ni una superior, el comando `gpg --full-generate-key` no funciona. Copia el siguiente texto y continúa con el paso 6.
      ```shell{:copy}
      $ gpg --default-new-key-algo rsa4096 --gen-key
      ```
4. En el prompt, especifica la clase de llave que quieres, o presiona `Enter` para aceptar lo predeterminado.
5. En el prompt, especifica el tamaño de llave que quieres, o presiona `Enter` para aceptar lo predeterminado. Tu llave debe ser de al menos `4096` bits.
6. Ingresa el periodo de validez que deberá tener la llave. Presiona `Enter` para especificar la selección predeterminada, indicando que la llave no expira. A menos de que requieras una fecha de vencimiento, te recomendamos aceptar esta característica predeterminada.
7. Verifica que tus selecciones sean correctas.
8. Ingresa tu información de ID de usuario.

  {% note %}

  **Nota:** Cuando se te pida que ingreses tu dirección de correo electrónico, asegúrate de ingresar la dirección de correo electrónico verificada para tu cuenta Github. {% data reusables.gpg.private-email %} {% ifversion fpt or ghec %}  Para obtener más información, consulta "[Verificar tu dirección de correo electrónico](/articles/verifying-your-email-address)" and "[Establecer tu dirección de correo electrónico para confirmaciones](/articles/setting-your-commit-email-address)".{% endif %}

  {% endnote %}

9. Escribe una contraseña segura.
{% data reusables.gpg.list-keys-with-note %}
{% data reusables.gpg.copy-gpg-key-id %}
10. Pega el siguiente texto sustituyendo el ID de la llave GPG que deseas usar. En este ejemplo, el ID de la llave GPG es `3AA5C34371567BD2`:
 ```shell{:copy}
 $ gpg --armor --export 3AA5C34371567BD2
 # Prints the GPG key ID, in ASCII armor format
 ```
11. Copia tu llave GPG, comenzando con `-----BEGIN PGP PUBLIC KEY BLOCK-----` y terminando con `-----END PGP PUBLIC KEY BLOCK-----`.
12. [Agrega la llave GPG a tu cuenta de GitHub](/articles/adding-a-gpg-key-to-your-github-account).

## Leer más

* "[Comprobar llaves GPG existentes](/articles/checking-for-existing-gpg-keys)"
* "[Agregar una llave GPG a tu cuenta de GitHub](/articles/adding-a-gpg-key-to-your-github-account)"
* "[Informar a Git sobre tu llave de firma](/articles/telling-git-about-your-signing-key)"
* "[Asociar un correo electrónico con tu llave GPG](/articles/associating-an-email-with-your-gpg-key)"
* "[Firmar confirmaciones](/articles/signing-commits)"
* "[Firmar etiquetas](/articles/signing-tags)"
