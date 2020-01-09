# Anpassungen im Code für WiBU GDPR-Compliance

  ### Datei sidebar-default.php

  Einbau des neuen CookieConsent oberhalb von `<div id="serviceBar">`.

```
  <div data-sticky-container>
    <div class="sticky top-bar" data-sticky data-margin-top="0" data-sticky-on="small">

      **Pfad zur Datei im Template: wibu-theme/templates/partials/gdpr/cookieconsent.php**
-->		<?php get_template_part( PARTIALS . 'gdpr/cookieconsent') ?>

      <div id="serviceBar">
```
