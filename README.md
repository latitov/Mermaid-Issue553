# Mermaid-Issue553
A solution to the Issue 553, how to embed Mermaid diagram into the md files of Github.

```mermaid
graph LR
   A --> B
   A -->C
   C -->D
```

## Problem Context

People asked for almost a decade for support of Mermaid syntax in the GitHub. Unfortunatelly, these beareucrats ignored the Issue 553 request, and then closed it with no comment. Despite all they needed to do, was to add less than 10 lines of code.

## Possible solutions:

### Use Jekyll + TeXt theme

Jekyll is a simple, blog-aware, __static site generator__ for personal, project, or organization sites. Written in Ruby by Tom Preston-Werner, GitHub's co-founder, it is distributed under the open source MIT license.

https://jekyllrb.com/

https://tianqi.name/jekyll-TeXt-theme/docs/en/quick-start

DOWNSIDE:

It only applicable if you maintain your own installation (self-host the site), and won't work for public GitHub.

### Use browser plugin

https://stackoverflow.com/a/64695218/11729048

https://addons.mozilla.org/en-US/firefox/addon/github-mermaid/?src=recommended

How this works: it just loads a mermaid.js into yor document, so any div of class "mermaid" gets processed.
 
DOWNSIDE:

It won't show diagrams for people visiting the page, who don't have that plugin installed.

## This page, as seen when the plugin is installed

![](1.svg)

## Example

```mermaid
classDiagram
    Animal <|-- Duck
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
      +String beakColor
      +swim()
      +quack()
    }
    class Fish{
      -int sizeInFeet
      -canEat()
    }
    class Zebra{
      +bool is_wild
      +run()
    }
    
```
```mermaid
graph LR
   A --> B
   A -->C
   C -->D
```

```mermaid
erDiagram
          CUSTOMER }|..|{ DELIVERY-ADDRESS : has
          CUSTOMER ||--o{ ORDER : places
          CUSTOMER ||--o{ INVOICE : "liable for"
          DELIVERY-ADDRESS ||--o{ ORDER : receives
          INVOICE ||--|{ ORDER : covers
          ORDER ||--|{ ORDER-ITEM : includes
          PRODUCT-CATEGORY ||--|{ PRODUCT : contains
          PRODUCT ||--o{ ORDER-ITEM : "ordered in"
```


![pic2](pic2.png)

