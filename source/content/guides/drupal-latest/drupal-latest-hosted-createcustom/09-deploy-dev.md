---
title: Migrate a Custom Upstream to Drupal:latest
subtitle: Deploy to Dev
description: 
<<<<<<< HEAD:source/content/guides/drupal-latest/drupal-latest-hosted-createcustom/09-deploy-dev.md
cms: "Drupal"
=======
cms: "Drupal:latest"
>>>>>>> eec42263af4cf5e002bae842ccae64ea51704a74:source/content/guides/drupal-latest/drupal-latest-hosted-createcustom/09-deploy-dev.md
tags: [code, launch, migrate, site, updates, D8, D9, D10]
contributors: [wordsmither, michellecolon-pantheon]
layout: guide
permalink: docs/guides/drupal-latest-hosted-createcustom/deploy-dev
anchorid: deploy-dev
editpath: drupal-latest/drupal-latest-hosted-createcustom/09-deploy-dev.md
reviewed: "2022-12-12"
contenttype: [guide]
categories: [migrate, git]
newcms: [drupal, drupal8, drupal9, drupal10]
audience: [development]
product: [dashboard, custom-upstreams]
integration: [--]
---

Merge the code and files from the Multidev environment to the Dev environment.

1. Merge the `composerify` branch on the Custom Upstream into the `master` branch and push:

    ```bash{promptUser:user}
    git checkout master
    git merge composerify && git push origin master
    ```

1. Apply the upstream updates to your individual sites. This will only apply them to the Dev environment.

1. If you applied any site-specific code to individual sites' `ic-test` Multidev, merge that Multidev into the Dev environment.

  <Alert title="Note" type="info" >

  There is currently a platform bug which prevents Integrated Composer from being enabled until a change to `pantheon.yml` has been pushed to *each site*. Follow the steps below to complete the final deployment.

  </Alert>

1. After you push to Dev, you must push another change to `pantheon.yml`. You can either:

    - Add a comment in `pantheon.yml` at the end of the file, and that will trigger Composer

      Or

    - Use `echo` to do it for you:

     ```bash{promptUser:user}
     echo "\n# comment to trigger Composer\n" >> pantheon.yml
     ```

1. Make sure to push your changes up again.

1. Confirm that the Dev environment is working as expected.