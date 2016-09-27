add .bind to a property

compose

    view="some.html"
    
    view-model="some-model.js"
    
        _if missing then uses the parent vm_
        
 
 ```html
<div repeat.for="event of events">
    <compose model.bind="event" view-model="event"></compose>
</div>
 ```
 
