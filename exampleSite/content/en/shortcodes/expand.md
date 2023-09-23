---
title: Expand
---

### expand


Expand shortcode can help to decrease clutter on screen by hiding part of text.  
Expand content by clicking on it.

Thanks to the deep exploration of [Nelis Oostens][nelis-oostens][^nelis-oostens], There's a 
{{< hint type="important" title="Quirks of Shortcode Behavior with markdown AND html!"  >}}

It's important to note that the impact of the above, is that most use cases of the **expand** shortcode will now require using the alternative shortcode invocation syntax: **{{\% %}}** in lieu of **{{\< >}}**.  
Please read the above link for a more in-depth explanation of the problem, and workaround.

{{< /hint >}}

{{% expand title="Full Parameter Description 📜" expanded=true symbol="⤵" %}}

*in positional order:*
##### title {#prmtitle}
`(String)` (Default: '**Expand**')  
  This sets the string displayed in the heading.  
  May contain emoji.

##### symbol {#prmsymbol}
`(String)` (Default: '**↕**')  
  The glyph, string, emoji, or other element 


##### expanded {#prmexpanded}
`(Bool)`  (Default: '**false**)
##### id {#prmid}
`(String)` (Default: '**[substr][substr] (sha1 .Inner) 0 8**'[^substr])

{{% /expand %}}

### Default

<!-- prettier-ignore-start -->
```tpl
{{%/* expand */%}}
## Markdown content
Dolor sit, sumo unique ...
{{%/* /expand */%}}
```
<!-- prettier-ignore-end -->

{{% expand %}}

## Markdown content

Dolor sit, sumo unique argument um no. Gracie nominal id xiv. Romanesque acclimates investiture. Ornateness bland it ex enc, est yeti am bongo detract re.
{{% /expand %}}

### With A Custom Label

<!-- prettier-ignore-start -->
```tpl
{{%/* expand "Custom Label" "..." */%}}
## Markdown content
Dolor sit, sumo unique ...[^note]


{{%/* /expand */%}}
```

```tpl
{{%/* expand title="Named Custom Label" symbol="⤵" */%}}
## Markdown content
Dolor sit, sumo unique ... [^note]
{{%/* /expand */%}}
```


<!-- prettier-ignore-end -->

{{% expand "Custom Label" "..." %}}
## Markdown content
Dolor sit, sumo unique ...[^note]

{{% /expand %}}

{{% expand title="Named Custom Label" symbol="⤵" %}}
## Markdown content
Dolor sit, sumo unique ...[^note]

{{% /expand %}}

### Default Open With Custom Label

<!-- prettier-ignore-start -->
```tpl
{{%/* expand "Custom Label" "..." true */%}}
## Markdown content
Dolor sit, sumo unique ...
[Who is this lorem ipsum fellow?][lorem][^lorem]

{{%/* /expand */%}}
```

```tpl
{{%/* expand title="Custom Label" symbol="..." expanded=true */%}}
## Markdown content
Dolor sit, sumo unique ...
[Who is this lorem ipsum fellow?][lorem][^lorem]

{{%/* /expand */%}}
```
<!-- prettier-ignore-end -->

{{% expand title="Custom Label" symbol="..." expanded=true %}}

## More markdown

[Who is this lorem ipsum fellow?][lorem][^lorem]  
Dolor sit, sumo unique argument um no. Gracie nominal id xiv. Romanesque acclimates
investiture. Ornateness bland it ex enc, est yeti am bongo detract re. Pro ad prompts
feud gait, quid exercise emeritus bis e. In pro quints consequent, denim fastidious
copious quo ad. Stet probates in duo.
{{% /expand %}}

[nelis-oostens]: <https://oostens.me/posts/hugo-shortcodes-with-markdown-gotchas/>
[ordinal]: <https://gohugo.io/variables/shortcodes/#prose>
[substr]: <https://gohugo.io/functions/substr/>
[lorem]: <https://en.wikipedia.org/wiki/Lorem_ipsum>

[^lorem]: <https://en.wikipedia.org/wiki/Lorem_ipsum>
[^note]: **Note to self**: Don't get attached to quirky features... The Yak Shaving propensity is high.
[^substr]: <https://gohugo.io/functions/substr/>
[^ordinal]: <https://gohugo.io/variables/shortcodes/#prose>
[^nelis-oostens]: <https://oostens.me/posts/hugo-shortcodes-with-markdown-gotchas/>