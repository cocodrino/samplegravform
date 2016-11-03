---
title: Net4Email
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
    action: /
    name: contactanos
    fields:
    -
        name: nombre
        label: Nombre
        placeholder: 'Ingrese su Nombre'
        autofocus: 'on'
        autocomplete: 'on'
        type: text
        
    buttons:
    -
        type : submit
        value : Enviar
    
    process:
    -
        message: "gracias por contactarnos"
---


