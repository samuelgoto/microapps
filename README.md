---
permalink: index.html
---

microapps is an early **proposal** to extend [schema.org](https://schema.org) with a presentation-based markup language (akin to HTML) that enables creating domain-agnostic interactable snippets in search engines (i.e. within their security and consistency constrains).

The XML-based notation is designed to de-couple application-specific factual semantics in schema.org (e.g. [restaurants](http://schema.org/Restaurant), [museums](http://schema.org/Museum), [people](http://schema.org/Person) and [actions](http://schema.org/Action)) with general-purpose presentation building blocks (e.g. paragraphs, text formatting, lists, headers, footers and forms), while still enabling their association.

```xml
<doc itemscope itemtype="http://schema.org/Restaurant">
  <title itemprop="name">Sam's restaurant</title>
  <p itemprop="description">Welcome to my restaurant!</p>
  <form itemprop="potentialAction" 
    itemscope
    itemtype="http://schema.org/ReserveAction"
    action="/create.php">
    <label for="name"></label>
    <input itemprop="agent name" name="name"></input>
    <input type="button"></input>
  </form>
</doc>
```

The elements are designed to be as compatible as possible to (and to resemble as much as possible) HTML. Unlike HTML, microapps elements operate under an environment (i.e. search engine results pages) with stricter requirements of styling consistency (e.g. they don't allow CSS) and scripting (e.g. no JS), increasing their embedability at the cost of their expressivity.

