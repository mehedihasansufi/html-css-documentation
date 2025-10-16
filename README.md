# Html-documentation

<!-- Semantic tag -->

### Semantic & Non-Semantic tag

<hr/><br>

```html
<!-- Semantic -->

- header,footer,main,form,table

<!-- Non-Semantic  -->
- div,span,
```

<!-- form part here -->

## Form

```html
<!-- form tag is mandatory -->

<form>
  <!-- simple input form -->

  <input type="text" />

  <!-- requird means user must fill up the box -->

  <input type="text" requird/>
  <input type="email" requird/>
  <input type="password" requird/>

  <!-- with label -->

    <label for="id from the input id">before text input box<label>
    <input type="text" id="username" name="must be same of the id"/>
</form>
```

### button 

```html
<form>

    <button type="submit"></button>
    <button type="reset">for clear the data from the input box</button>
</form>
```

### text area

```html
<label for="same as the id">Some text</label>
<textarea name="same as the id" id="" cols="" rows=""></textarea>
```

  <!-- Table part here -->

## Table

```html
<table>
  <thead>
    <tr>
      <th>table heading</th>
      <th>table heading 2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>table data</td>
      <td>table data 2</td>
    </tr>
  </tbody>
</table>
```

<!-- Text formating part -->

#### text formating tag

```html
<strong>fot text bold</strong>

<em>itlic</em>

<mark>highlight</mark>

<del>deleted text</del>

<u>underline</u>

(a+b)<sup>2</sup>
```

<!-- Listing area part -->

### list

<hr/><br>

1.  Order list
2.  Unorder list
3.  Defination list

<!--Oeder list -->

#### Order list

```html
<ol type="1" start="5" reversed>
  <!-- if we want to change with attribute (type),(start),(reversed) -->

  <li>html</li>
  <li>css</li>
  <li>javascript</li>
</ol>
```

<!--Defination list -->

#### Defination List

```html
<dl>
  <dt>html</dt>
  <!-- difination title -->
  <dd>Hyper Text Markup Language</dd>
  <!-- defination data-->
</dl>
```

<!-- Linking area here -->

## Link

2 types of link

- absulate path
- relative path

```html
<!-- target attribute "_blank" use for the link with new tab -->

<a target="_blank" href="there will be link"
  >there is a name that you want to display</a
>
```

Title attribute use

```html
<!-- (title)---attribute use, when we hober some text will be show -->

<a href="link" title="hyper text markup language">html</a>
```

For Phone number & Email attribute

```html
<a href="tel:01768......">call me</a>
<!-- for emal -->
<a href="mailto:example@gmail.com">Email</a>
```

#### horizontal rule

```html
<hr />
```
