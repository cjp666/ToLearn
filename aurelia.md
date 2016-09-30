add .bind to a property
    repeat.for
    show.bind
    if.bind
    href.bind
    class.bind

compose

    view="some.html"
    
    view-model="some-model.js"
    
        (if missing then uses the parent vm)
        
 
 ```html
<div repeat.for="event of events">
    <compose model.bind="event" view-model="event"></compose>
</div>
 ```
 
Make a div editable

```html
<div textContext.bind="event.description" contenteditable="true"></div>
```

Use click.delegate rather than click.trigger

## Working with \<select\>

### Binding to strings
```html
<select id="state" value.bind="job.location.state">
   <option repeat.for="state of states" value.bind="state">${state}</option>
</select>
```

### Binding to objects
```html
<select id="state" value.bind="job.location.state">
    <option repeat.for="state in states" model.bind="state.abbreviation">${state.name}</option>
</select>
```

