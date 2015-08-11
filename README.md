# Generate an URL list from an angular router for the Google sitemap generator

## Introduction

This small AWK script parses the static routes defined in a
`routes.js` angular JS router and creates an URL list to be used by
the
[google sitemap generator](https://code.google.com/p/googlesitemapgenerator/).

## Usage

    awk -v domain="http://example.com" -v frequency="daily" -v priority=0.8 -f angular-generate-urls.awk routes.js 

Prints the url list in stdout with the specified frequency and
priority. The output can directed to a file:

        awk -v domain="http://example.com" -v frequency="daily" -v priority=0.8 -f angular-generate-urls.awk routes.js > url_list.txt

in this case it writes the output to `url_list.txt`. The `frequency`
and `priority` are optional variables for the AWK script.

The URL list file can be edited for further customization.
