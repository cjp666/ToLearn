add .bind to a property
    repeat.for
    show.bind
    if.bind
    href.bind
    class.bind

compose

    view="some.html"
    
    view-model="some-model.js"
    
        _if missing then uses the parent vm_
        
 
 ```html
<div repeat.for="event of events">
    <compose model.bind="event" view-model="event"></compose>
</div>
 ```
 
