---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: false
type: "page"
menu: 
  main:
    name: "{{ replace .Name "-" " " | title }}"
    weight: 1
    
---

