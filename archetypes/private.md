---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
outputs: ["HTML"]
sitemap:
  disable: true
build:
  list: local
  render: true
  publishResources: true
---

