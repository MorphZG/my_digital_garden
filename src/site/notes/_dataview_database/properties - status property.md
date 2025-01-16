---
{"dg-publish":true,"permalink":"/dataview-database/properties-status-property/","title":"Status property","tags":["dataview","index"]}
---


# Status property

Stage of maturity or completeness of a note. Available values: `draft`, `useful`, `detailed`, `master`

#### Status: draft

- Notes still in a form of a placeholder or not not really useful. Provides zero value.

>[!quote]- dataview query
>
>  | File | status |
> | ---- | ------ |
> 
{ .block-language-dataview}

#### Status: useful

- Notes providing enough value to be useful.

>[!quote]- dataview query
>
>  | File | status |
> | ---- | ------ |
> 
{ .block-language-dataview}

#### Status: detailed

- Very detailed notes with more than enough information.

>[!quote]- dataview query
>
>  | File | status |
> | ---- | ------ |
> 
{ .block-language-dataview}

#### Status: master

- Notes with "detailed" status will become "master" notes after being reviewed and analysed more than once.

>[!quote]- dataview query
>
>  | File | status |
> | ---- | ------ |
> 
{ .block-language-dataview}
