# Anpassungen im Code für WiBU GDPR-Compliance

  ### Datei sidebar-default.php

  Einbindung des neuen CookieConsent oberhalb von `<div id="serviceBar">`.
  Pfad zur Datei im Template: `wibu-theme/templates/partials/gdpr/cookieconsent.php`

```
    <div class="sticky top-bar" data-sticky data-margin-top="0" data-sticky-on="small">

-->		<?php get_template_part( PARTIALS . 'gdpr/cookieconsent') ?>

      <div id="serviceBar">
```

  ### CSS für den neuen Cookie Disclaimer

  Als SASS für Foundation 6

```css
  #cookieConsent {
    background: $dust;
    transition: height .4s ease;
    overflow: hidden;

    & > div {
      margin:0 -10px;
      @include xy-gutters($grid-large-container-padding,padding,top bottom left right,false);

      @include breakpoint(xmedium) {
        margin:0 -30px;
      }
      @include breakpoint($menu-break-mobile) {
        margin:0 -40px;
        @include xy-gutters($blockgrid-gutters,padding,top bottom,false);

      }
    }

    .grid-x {
      max-width: rem-calc(1370);
      margin: 0 auto;
    }

    .cell.xmedium-9 {
      @include breakpoint(xmedium) {
        @include xy-gutters($small-vertical-inset-padding,padding,right,false);
      }
    }

    p {
      margin-bottom: 1em;
      font-size: rem-calc(14);
      @include breakpoint(medium) {
        font-size: rem-calc(14);
      }
      @include breakpoint(xmedium) {
        margin-bottom:0;
      }

      &.h2 {
        font-size: rem-calc(16);
        margin-bottom: 1em;
      }
    }

    .button-group {
      margin:0 -0.5rem;
      @include breakpoint(xmedium) {
        flex-wrap: wrap;
        margin:5px 0 0;
      }
      .button {
        font-size: 0.8rem !important;
        margin:0 0.5rem;
        @include breakpoint(xmedium) {
          flex: 0 0 100%;
          margin:0 0 0.5rem;
        }
      }
    }
  }

  .button-group.gasettings {
    @include breakpoint(medium) {
      margin:0 -0.5rem;
    }
    .button {
      @include breakpoint(medium) {
        margin:0 0.5rem;
        max-width: 250px;
      }
    }
  }

  .yt-disclaimer {
    position: absolute;
    bottom:0;
    background-color:rgba(37,77,109,0.7);
    color:$white;
    @include xy-gutters($small-vertical-inset-padding, padding, top bottom, false);
    transition: padding-bottom .4s ease;

    .cell {
      @include xy-gutters($small-vertical-inset-padding, padding, left right, false);
    }
    .grid-x {
      margin:0 !important;
    }
    p {
      margin-bottom: 1em;
      font-size: rem-calc(12);
      @include breakpoint(medium) {
        font-size: rem-calc(14);
      }
      @include breakpoint(xmedium) {
        margin-bottom:0;
      }
    }
  }
    .yt-disc-play {
      position: absolute;
      width: 94px;
      height: 69px;
      left: 50%;
      top: 50%;
      margin-top: -35px;
      margin-left: -47px;
    }

```

  Als Compiliertes CSS

```css
#cookieConsent {
  background: #EBEBEB;
  transition: height .4s ease;
  overflow: hidden; }
  #cookieConsent > div {
    margin: 0 -10px;
    padding-top: 0.9375rem;
    padding-bottom: 0.9375rem;
    padding-left: 0.9375rem;
    padding-right: 0.9375rem; }
    @media print, screen and (min-width: 56.25em) {
      #cookieConsent > div {
        padding-top: 1.875rem;
        padding-bottom: 1.875rem;
        padding-left: 1.875rem;
        padding-right: 1.875rem; } }
    @media print, screen and (min-width: 56.25em) {
      #cookieConsent > div {
        margin: 0 -30px; } }
    @media screen and (min-width: 64em) {
      #cookieConsent > div {
        margin: 0 -40px;
        padding-top: 0.3125rem;
        padding-bottom: 0.3125rem; } }
  @media screen and (min-width: 64em) and (min-width: 40em) {
    #cookieConsent > div {
      padding-top: 0.625rem;
      padding-bottom: 0.625rem; } }
  @media screen and (min-width: 64em) and (min-width: 56.25em) {
    #cookieConsent > div {
      padding-top: 0.9375rem;
      padding-bottom: 0.9375rem; } }
  #cookieConsent .grid-x {
    max-width: 85.625rem;
    margin: 0 auto; }
  @media print, screen and (min-width: 56.25em) {
    #cookieConsent .cell.xmedium-9, #cookieConsent .downloads-archive .xmedium-9.list-element, .downloads-archive #cookieConsent .xmedium-9.list-element {
      padding-right: 1.25rem; } }
  @media print, screen and (min-width: 56.25em) and (min-width: 40em) {
    #cookieConsent .cell.xmedium-9, #cookieConsent .downloads-archive .xmedium-9.list-element, .downloads-archive #cookieConsent .xmedium-9.list-element {
      padding-right: 1.875rem; } }
  #cookieConsent p {
    margin-bottom: 1em;
    font-size: 0.875rem; }
    @media print, screen and (min-width: 40em) {
      #cookieConsent p {
        font-size: 0.875rem; } }
    @media print, screen and (min-width: 56.25em) {
      #cookieConsent p {
        margin-bottom: 0; } }
    #cookieConsent p.h2 {
      font-size: 1rem;
      margin-bottom: 1em; }
  #cookieConsent .button-group {
    margin: 0 -0.5rem; }
    @media print, screen and (min-width: 56.25em) {
      #cookieConsent .button-group {
        -webkit-flex-wrap: wrap;
            -ms-flex-wrap: wrap;
                flex-wrap: wrap;
        margin: 5px 0 0; } }
    #cookieConsent .button-group .button, #cookieConsent .button-group .page-pagination a, .page-pagination #cookieConsent .button-group a, #cookieConsent .button-group .reference-pager .pods-pagination-paginate a, .reference-pager .pods-pagination-paginate #cookieConsent .button-group a, #cookieConsent .button-group .page-pagination span, .page-pagination #cookieConsent .button-group span, #cookieConsent .button-group .reference-pager .pods-pagination-paginate span, .reference-pager .pods-pagination-paginate #cookieConsent .button-group span, #cookieConsent .button-group .wpcf7-submit {
      font-size: 0.8rem !important;
      margin: 0 0.5rem; }
      @media print, screen and (min-width: 56.25em) {
        #cookieConsent .button-group .button, #cookieConsent .button-group .page-pagination a, .page-pagination #cookieConsent .button-group a, #cookieConsent .button-group .reference-pager .pods-pagination-paginate a, .reference-pager .pods-pagination-paginate #cookieConsent .button-group a, #cookieConsent .button-group .page-pagination span, .page-pagination #cookieConsent .button-group span, #cookieConsent .button-group .reference-pager .pods-pagination-paginate span, .reference-pager .pods-pagination-paginate #cookieConsent .button-group span, #cookieConsent .button-group .wpcf7-submit {
          -webkit-flex: 0 0 100%;
              -ms-flex: 0 0 100%;
                  flex: 0 0 100%;
          margin: 0 0 0.5rem; } }

@media print, screen and (min-width: 40em) {
  .button-group.gasettings {
    margin: 0 -0.5rem; } }

@media print, screen and (min-width: 40em) {
  .button-group.gasettings .button, .button-group.gasettings .page-pagination a, .page-pagination .button-group.gasettings a, .button-group.gasettings .reference-pager .pods-pagination-paginate a, .reference-pager .pods-pagination-paginate .button-group.gasettings a, .button-group.gasettings .page-pagination span, .page-pagination .button-group.gasettings span, .button-group.gasettings .reference-pager .pods-pagination-paginate span, .reference-pager .pods-pagination-paginate .button-group.gasettings span, .button-group.gasettings .wpcf7-submit {
    margin: 0 0.5rem;
    max-width: 250px; } }

.yt-disclaimer {
  position: absolute;
  bottom: 0;
  background-color: rgba(37, 77, 109, 0.7);
  color: #ffffff;
  padding-top: 1.25rem;
  padding-bottom: 1.25rem;
  transition: padding-bottom .4s ease; }
  @media print, screen and (min-width: 40em) {
    .yt-disclaimer {
      padding-top: 1.875rem;
      padding-bottom: 1.875rem; } }
  .yt-disclaimer .cell, .yt-disclaimer .downloads-archive .list-element, .downloads-archive .yt-disclaimer .list-element {
    padding-left: 1.25rem;
    padding-right: 1.25rem; }
    @media print, screen and (min-width: 40em) {
      .yt-disclaimer .cell, .yt-disclaimer .downloads-archive .list-element, .downloads-archive .yt-disclaimer .list-element {
        padding-left: 1.875rem;
        padding-right: 1.875rem; } }
  .yt-disclaimer .grid-x {
    margin: 0 !important; }
  .yt-disclaimer p {
    margin-bottom: 1em;
    font-size: 0.75rem; }
    @media print, screen and (min-width: 40em) {
      .yt-disclaimer p {
        font-size: 0.875rem; } }
    @media print, screen and (min-width: 56.25em) {
      .yt-disclaimer p {
        margin-bottom: 0; } }

.yt-disc-play {
  position: absolute;
  width: 94px;
  height: 69px;
  left: 50%;
  top: 50%;
  margin-top: -35px;
  margin-left: -47px; }
```
