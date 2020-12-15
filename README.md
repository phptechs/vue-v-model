# v-model docs

## text types (text, password, textarea)

Uses `value` property and `@input` event

### Native element

```html
<!-- shorthand -->
<input v-model="something" />
<!-- expanded -->
<input :value="something" @input="something = $event.target.value" />
```

### Parent-child

```html
<!-- parent -->
<Child v-model:something="something"></Child>
<!-- child -->
<input :value="something" @input="$emit('update:something', $event.target.value)" />
```

## Checkbox and radio

Uses `checked` property and `@change` event

### Native element

```html
<!-- shorthand -->
<input v-model="something" />
<!-- expanded -->
<input :checked="something" @change="something = $event.target.checked" />
```

### Parent-child

```html
<!-- parent -->
<Child v-model:something="something"></Child>
<!-- child -->
<input :checked="something" @change="$emit('update:something', $event.target.checked)" />
```

## Select

Uses `value` property and `@change` event

### Native element

```html
<!-- shorthand -->
<select v-model="selected">
  <option disabled value="">Please select one</option>
  <option>A</option>
  <option>B</option>
  <option>C</option>
</select>
<!-- expanded -->
<select :value="something" @change="something = $event.target.value" />
```

### Parent-child

```html
<!-- parent -->
<Child v-model:something="something"></Child>
<!-- child -->
<select :value="something" @change="$emit('update:something', $event.target.value)" />
```
