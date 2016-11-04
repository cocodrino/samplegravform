---
title: net4email
menu: Home
onpage_menu: true
body_class: index
header_class: alt
content:
    items: @self.modular
    order:
        by: default
        dir: asc
        custom:
            - _banner
            - _icons
            - _header
            - _features
            - _portfolio
            - _contact

form:
    action: /home
    name: contacto
    fields:
    -
        name: nombre
        label: Nombre
        placeholder: 'Ingrese ambos nombres'
        autofocus: 'on'
        autocomplete: 'on'
        type: text
        
    -
        name: apellido
        label: Apellido
        type: text
        
    -
        name: correo
        label: Correo Electrónico
        type: email
        validate:
            required : true
        
    - 
      name: telefono
      label: Telefono
      placeholder: 212-222-2222
      type: text
    
    buttons:
    -
        type : submit
        value : Enviar
    
    process:
        - email:
            from: "clagccs@gmail.com"
            to: "{{ form.value.correo }}"
            subject: "[Feedback] {{ form.value.nombre }}"
            body: "FUNCIONO BIEN!!"
        - message: Thank you for your feedback!
        - display: thankyou
---


