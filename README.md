# WildVerse Media CDN

This repository serves as the media delivery layer for the WildVerse platform.

Rather than storing album artwork and thumbnails directly on the production hosting environment, WildVerse uses GitHub Pages as a lightweight media CDN for static assets.

## Purpose

The repository stores:

* Album artwork
* Artist artwork
* Thumbnails
* Persona images
* WebP optimized assets
* Media manifests

Assets are deployed automatically and served through GitHub infrastructure.

## Why This Architecture?

Traditional music websites often store all images directly on the web server.

WildVerse separates responsibilities:

| Component    | Responsibility          |
| ------------ | ----------------------- |
| Hostinger    | Website frontend        |
| MariaDB      | Metadata storage        |
| VPS Node.js  | Media processing        |
| FFmpeg       | Audio sprite extraction |
| GitHub Pages | Static image delivery   |

This reduces storage pressure on the production server while improving deployment flexibility.

## Artwork Pipeline

The workflow is:

1. Create or receive artwork
2. Convert to optimized WebP format
3. Push to GitHub repository
4. Deploy automatically through GitHub Pages
5. Store asset URL in MariaDB
6. Serve artwork through public CDN-style URLs

No manual image uploads are required on the production server.

## Related Project

WildVerse

https://wildverse.codbiohub.com

An experimental creator platform combining:

* Music
* Sound effects
* Audio sprites
* Persona-driven discovery
* On-demand media generation
* Metadata-driven content delivery

## Author

Wilder Ruiz
Finland / Bolivia
Bioinformatician, software developer, and creator.
