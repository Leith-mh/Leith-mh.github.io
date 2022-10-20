---
# An instance of the Experience widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: experience

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 40

title: Experience
subtitle:

# Date format for experience
#   Refer to https://wowchemy.com/docs/customization/#date-format
date_format: Jan 2006

# Experiences.
#   Add/remove as many `experience` items below as you like.
#   Required fields are `title`, `company`, and `date_start`.
#   Leave `date_end` empty if it's your current employer.
#   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
experience:
  - title: Devops Administrator
    company: Cremoetry
    company_url: ''
    company_logo: ''
    location: Remote
    date_start: '2022-06-01'
    date_end: '2022-09-15'
    description: |2-
        Responsibilities include:
        
        * Administrating a distributed kubernetes cluster
        * Ensure inter-nodes communications between a heterogeneous cloudand on premise environment using netmaker and wireguard.
        * Developing a GoLang script to query relevant kubernetes usage metrics using client-go library.
        * Implementation of an EKS and a GKE cluster
        * Provisioning infrastructure with terraform
        * Dockernization of applications (go,node)
        * Using open-cost datadog and Promethus to monitor kb8 clus
  - title: web developer
    company: Freelance
    company_url: ''
    company_logo: ''
    location: ''
    date_start: '2022-02-01'
    date_end: '2022-05-15'
    description: developing and deploying a webapp for a tunisian travel agency
  
  - title: Web developer intern
    company: ProxymIT
    company_url: ''
    company_logo: ''
    location: Sousse
    date_start: '2021-08-01'
    date_end: '2021-10-01'
    description: |2- 
      Developing a Driving school management system web app using React JS for the front end and spring boot for the backed and postgreSQL as the database

design:
  columns: '2'
---
