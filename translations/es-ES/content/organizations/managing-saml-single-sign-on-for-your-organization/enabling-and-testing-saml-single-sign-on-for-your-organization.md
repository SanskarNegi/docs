---
title: Habilitar y probar el inicio de sesión único SAML para tu organización
intro: Los administradores y los propietarios de la organización pueden habilitar el inicio de sesión único SAML para agregar una capa más de seguridad a su organización.
redirect_from:
  - /articles/enabling-and-testing-saml-single-sign-on-for-your-organization
  - /github/setting-up-and-managing-organizations-and-teams/enabling-and-testing-saml-single-sign-on-for-your-organization
versions:
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Habilitar & probar el SSO de SAML
---

## Acerca del inicio de sesión único de SAML

Puedes habilitar SAML SSO (inicio de sesión único) en tu organización sin requerir que todos los miembros lo usen. Habilitar pero no exigir SAML SSO en tu organización puede facilitar la adopción de SAML SSO por parte de la organización. Una vez que la mayoría de los miembros usen SAML SSO, podrás exigirlo en toda la organización.

{% data reusables.saml.ghec-only %}

Si habilitas pero no exiges SAML SSO, los miembros de la organización que elijan no usar SAML SSO pueden seguir siendo miembros de esta. Para obtener más información acerca de la exigencia de SAML SSO, consulta "[Exigir inicio de sesión único SAML para tu organización](/articles/enforcing-saml-single-sign-on-for-your-organization)".

{% data reusables.saml.outside-collaborators-exemption %}

{% data reusables.saml.saml-disabled-linked-identities-removed %}

## Habilitar y probar el inicio de sesión único SAML para tu organización

Antes de requerir el SSO de SAML en tu organización, asegúrate de que la hayas preparado. Para obtener más información, consulta "[Preparación para exigir inicio de sesión único SAML en tu organización](/articles/preparing-to-enforce-saml-single-sign-on-in-your-organization)".

Para obtener más información sobre los proveedores de identidad (IdP) que son compatibles con {% data variables.product.company_short %} para el SSO de SAML, consulta la sección "[Conectar tu proveedor de identidad a tu organización](/organizations/managing-saml-single-sign-on-for-your-organization/connecting-your-identity-provider-to-your-organization)".

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.security %}
5. En "inicio de sesión único SAML", selecciona **Habilitar autenticación SAML**. ![Casilla de verificación para habilitar SAML SSO](/assets/images/help/saml/saml_enable.png)

  {% note %}

  **Nota:** Luego de habilitar SAML SSO, puedes descargar tus códigos de recuperación de inicio de sesión único para poder acceder a tu organización aun cuando tu IdP no se encuentre disponible. Para obtener más información, consulta "[Descargar los códigos de recuperación de inicio de sesión único SAML de tu organización](/articles/downloading-your-organization-s-saml-single-sign-on-recovery-codes)".

  {% endnote %}

6. En el campo "URL de inicio de sesión único", escribe el extremo del HTTPS de tu IdP para las solicitudes de inicio de sesión único. Este valor se encuentra en la configuración de tu IdP. ![Campo para la URL a la que los miembros serán redireccionados cuando inicien sesión](/assets/images/help/saml/saml_sign_on_url.png)
7. También puedes escribir tu nombre de emisor SAML en el campo "Emisor". Esto verifica la autenticidad de los mensajes enviados. ![Campo para el nombre del emisor SAML](/assets/images/help/saml/saml_issuer.png)
8. En "Certificado público", copia un certificado para verificar las respuestas SAML. ![Campo para el certificado público de tu proveedor de identidad](/assets/images/help/saml/saml_public_certificate.png)
9. Haz clic en {% octicon "pencil" aria-label="The edit icon" %} y luego en los menús desplegables de Método de firma y Método de resumen y elige el algoritmo de hash que usa tu emisor SAML para verificar la integridad de las solicitudes. ![Menús desplegables para los algoritmos de hash del Método de firma y del Método de resumen usados por tu emisor SAML](/assets/images/help/saml/saml_hashing_method.png)
10. Antes de habilitar SAML SSO para tu organización, haz clic en **Probar la configuración de SAML** para asegurarte de que la información que has ingresado sea correcta. ![Botón para probar la configuración de SAML antes de exigir el inicio de sesión único](/assets/images/help/saml/saml_test.png)

  {% tip %}

  **Sugerencia:**{% data reusables.saml.testing-saml-sso %}

  {% endtip %}
11. Para implementar SAML SSO y eliminar a todos los miembros de la organización que no se hayan autenticado mediante tu IdP, selecciona **Require SAML SSO authentication for all members of the _organization name_ organization**.** (Requerir autenticación SAML SSO a todos los miembros de la organización [nombre de la organización]). Para obtener más información acerca de la exigencia de SAML SSO, consulta "[Exigir inicio de sesión único SAML para tu organización](/articles/enforcing-saml-single-sign-on-for-your-organization)". ![Casilla de verificación para requerir SAML SSO para tu organización ](/assets/images/help/saml/saml_require_saml_sso.png)</p></li>
12
Haz clic en **Save ** (guardar). ![Botón para guardar la configuración de SAML SSO](/assets/images/help/saml/saml_save.png)</ol>

## Leer más

- "[Acerca de la administración de identidad y el acceso con el inicio de sesión único de SAML](/articles/about-identity-and-access-management-with-saml-single-sign-on)"
- "[SAML configuration reference](/admin/identity-and-access-management/using-saml-for-enterprise-iam/saml-configuration-reference)"
