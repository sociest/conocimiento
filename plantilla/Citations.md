---
title: "{{title}}"
description: "{{#if abstract}}{{abstract}}{{/if}}"
permalink: "{{#if citekey}}{{citekey}}{{/if}}"
comments: true
publish: true
draft: false
enableToc: false
tags:
{{#if keywords}}
  {{#each keywords}}- "{{this}}"
  {{/each}}
{{/if}}
aliases:
{{#if citekey}}
  - "@{{citekey}}"
{{/if}}
cssclasses:
{{#if entry.type}}
  - "{{entry.type}}"
{{/if}}
socialDescription: "{{#if abstract}}{{abstract}}{{/if}}"
socialImage: "{{#if socialImage}}{{socialImage}}{{/if}}"
created: "{{issuedDate}}{{#if issuedTime}} {{issuedTime}}{{/if}}"
modified: "{{#if modified}}{{modified}}{{/if}}"
published: "{{#if issuedDate}}{{issuedDate}}{{/if}}"
---

<details>
<summary>📑 Metadatos</summary>

| Atributo           | Detalle  |
| ------------------ | -------- |
{{#each entry.data.fields}}
| {{@key}} | `{{this}}` |
{{/each}}

</details>

{{#if abstract}}

> ### 📄 Resumen
>
> {{abstract}}
> {{/if}}

{{#if entry.data.fields.note}}
> ### 🗒️ Notas
> {{entry.data.fields.note}}

{{/if}}



{{#if entry.links}}

> ### 🔗 Enlaces
>
> {{#each entry.links}}

- [{{#if this.title}}{{this.title}}{{else}}Enlace{{/if}}]({{this.url}})
  {{/each}}
  {{else}}
  {{#if URL}}
  > ### 🔗 Enlace
  >
  > [Ver online]({{URL}})
  > {{/if}}
  > {{/if}}

{{#if entry.files}}

> ### 📎 Archivos adjuntos
>
> {{#each entry.files}}

- [Archivo {{@index}}](file://{{this}})
  {{/each}}
  {{/if}}
