# v-model docs

## text types (text, password, textarea)

Should use `value` property and `@input` event

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

## Checkbox

Should use `checked` property and `@change` event

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
