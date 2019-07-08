## Examples

An input field looks like this.

```jsx { "props": { "className": "no-i18n" } }
<InputField
  type="text"
  :iconSet="['keyboard', '']"
  placeholder="How is CC Vocabulary?"
  value="It is awesome!"
  color="orange"
  is-basic/>
```

### Color set

An input field without color is grey.

```jsx { "props": { "className": "no-i18n" } }
<InputField
  type="text"
  placeholder="Answer..."/>
```

But in classic fashion, input fields can be colored with any color from the set 
provided by CC Vocabulary. Grey is nobody's favourite.

```jsx { "props": { "className": "no-i18n" } }
<InputField
  type="text"
  placeholder="Answer..."
  color="blue"/>
<br/><br/>
<InputField
  type="text"
  placeholder="Answer..."
  color="green"/>
<br/><br/>
<InputField
  type="text"
  placeholder="Answer..."
  color="magenta"/>
<br/><br/>
<InputField
  type="text"
  placeholder="Answer..."
  color="olive"/>
<br/><br/>
<InputField
  type="text"
  placeholder="Answer..."
  color="orange"/>
<br/><br/>
<InputField
  type="text"
  placeholder="Answer..."
  color="purple"/>
<br/><br/>
<InputField
  type="text"
  placeholder="Answer..."
  color="red"/>
<br/><br/>
<InputField
  type="text"
  placeholder="Answer..."
  color="sand"/>
<br/><br/>
<InputField
  type="text"
  placeholder="Answer..."
  color="yellow"/>
```

Also you may use one of the three shades, namely `light`, `dark` and `darker`, 
to accentuate the color.

```jsx { "props": { "className": "no-i18n" } }
<InputField
  type="text"
  placeholder="Answer..."
  color="blue"
  shade="light"/>
<br/><br/>
<InputField
  type="text"
  placeholder="Answer..."
  color="blue"/>
<br/><br/>
<InputField
  type="text"
  placeholder="Answer..."
  color="blue"
  shade="dark"/>
<br/><br/>
<InputField
  type="text"
  placeholder="Answer..."
  color="blue"
  shade="darker"/>
```

### Add-on set

A field can also contain two icons, one on the left and right side each. Note 
that the icon must be added to the FontAwesome library by the application.

```jsx { "props": { "className": "no-i18n" } }
<InputField
  type="text"
  :iconSet="['keyboard', '']"
  placeholder="Left"/>
<br/><br/>
<InputField
  type="text"
  :iconSet="['', 'keyboard']"
  placeholder="Right"/>
<br/><br/>
<InputField
  type="text"
  :iconSet="['keyboard', 'keyboard']"
  placeholder="Both"/>
```

If you'd like your own something there, you can override the left and the right
add-on slots with something you like.

```jsx { "props": { "className": "no-i18n" } }
<InputField
  type="text"
  placeholder="Not icons">
  <template v-slot:leftAddons>
    <div><strong>:-)</strong></div>
  </template>
  <template v-slot:rightAddons>
    <div><strong>:-(</strong></div>
  </template>
</InputField><br/><br/>
<InputField
  type="text"
  placeholder="License iconography">
  <template v-slot:leftAddons>
    <LicenseIconography :iconList="['']"/>
  </template>
  <template v-slot:rightAddons>
    <LicenseIconography :iconList="['by']"/>
  </template>
</InputField>
```

### Style set

An input field can be defined to not attract attention, unless given attention
via means of a focus.

```jsx { "props": { "className": "no-i18n" } }
<InputField
  type="text"
  :iconSet="['keyboard', '']"
  color="orange"
  is-basic
  placeholder="Answer"/>
``` 

### Size set

Input fields come in all sizes, from small to mega.

```jsx { "props": { "className": "no-i18n" } }
<InputField
  size="small"
  type="text"
  placeholder="Answer..."/>
<br/><br/>
<InputField
  type="text"
  placeholder="Answer..."/>
<br/><br/>
<InputField
  size="big"
  type="text"
  placeholder="Answer..."/>
<br/><br/>
<InputField
  size="large"
  type="text"
  placeholder="Answer..."/>
<br/><br/>
<InputField
  size="huge"
  type="text"
  placeholder="Answer..."/>
<br/><br/>
<InputField
  size="enormous"
  type="text"
  placeholder="Answer..."/>
<br/><br/>
<InputField
  size="gigantic"
  type="text"
  placeholder="Answer..."/>
<br/><br/>
<InputField
  size="mega"
  type="text"
  placeholder="Answer..."/>
<br/><br/>
```

### Indication set

A field may indicate erroneous input.

```jsx { "props": { "className": "no-i18n" } }
<InputField
  type="text"
  :iconSet="['keyboard', '']"
  placeholder="Answer..."
  value="Wrong answer"
  indication="negative"/>
```

A field may indicate correct input.

```jsx { "props": { "className": "no-i18n" } }
<InputField
  type="text"
  :iconSet="['keyboard', '']"
  placeholder="Answer..."
  value="Right answer"
  indication="positive"/>
```

### State set

A field may be disabled to prevent input altogether.

```jsx { "props": { "className": "no-i18n" } }
<InputField
  type="text"
  :iconSet="['keyboard', '']"
  placeholder="Answer..."
  value="Can't answer"
  is-disabled/>
```

### Attributes

All attributes that you could pass to an `input` tag can be passed to the 
`InputField` component. You've already seen the `placeholder` attribute in use 
above.

An initial `value` can be provided for the field.

```jsx { "props": { "className": "no-i18n" } }
<InputField
  type="text"
  value="Value"
  placeholder="Placeholder"
  color="olive"/>
```

The `type` attribute works as you would expect.

```jsx { "props": { "className": "no-i18n" } }
<InputField
  type="email"
  label="Email address?"
  placeholder="Email address..."
  color="blue">
</InputField><br/><br/>
<InputField
  type="url"
  label="Website URL?"
  placeholder="Website URL..."
  color="purple">
</InputField><br/><br/>
<InputField
  type="date"
  color="magenta">
</InputField><br/><br/>
<InputField
  type="time"
  color="orange">
</InputField><br/><br/>
<InputField
  type="file"
  color="yellow">
</InputField>
```