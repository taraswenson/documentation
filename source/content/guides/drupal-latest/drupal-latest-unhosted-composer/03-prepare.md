---
title: Migrate a Composer Managed Drupal:latest Site from Another Platform
subtitle: Prepare
description: 
<<<<<<< HEAD:source/content/guides/drupal-latest/drupal-latest-unhosted-composer/03-prepare.md
cms: "Drupal"
=======
cms: "Drupal:latest"
>>>>>>> eec42263af4cf5e002bae842ccae64ea51704a74:source/content/guides/drupal-latest/drupal-latest-unhosted-composer/03-prepare.md
tags: [code, launch, migrate, site, updates, composer, D8, D9, D10]
contributors: [wordsmither]
layout: guide
showtoc: true
permalink: docs/guides/drupal-latest-unhosted-composer/prepare
anchorid: prepare
editpath: drupal-latest/drupal-latest-unhosted-composer/03-prepare.md
reviewed: "2022-12-13"
contenttype: [guide]
categories: [migrate, create]
newcms: [drupal9, drupal8, drupal10, drupal]
audience: [development]
product: [composer]
integration: [--]
---

Complete all steps in this section to ensure that your site is ready to be migrated to Pantheon.

## Create a New drupal:latest Site

<Partial file="migrate/create-new-drupal-site.md" />

## Prepare the Local Environment

<Partial file="drupal-latest/prepare-local-environment-no-clone.md" />

### Create a Local Copy of the Old Site's Code

<Partial file="migrate/drupal-create-local.md" />

### Retrieve a Local Copy of the Pantheon Site's Code

<Partial file="migrate/d8composer-d8composer-requirements.md" />