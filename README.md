Tinymodal
============

Super tiny vanilla js module for modal windows. JS size 2290 bytes minified, 920 bytes gziped.


Main Ideas
----------
* No images, iframes, etc. Only html content
* Real modal window (no scrolling!)
* CSS should be outside code
* A11Y
* ~1-2kb of gziped JS+CSS are enough for modal window plugin
* There may be more than one modal window. Supports nested windows.
* Supports any modern browsers

Install
__________

```
    npm install tinymodal.js --save // via npm
    yarn add tinymodal.js --save // via yarn
```

Examples
----------


```html
<a href="#" id="some-link">Open popup</a>


<div class="modal modal-hidden" id="popup-example" aria-hidden="true">
    <div class="modal-content">
        <button class="modal-close" data-modal-close></button>

        Modal window content here.
        
    </div>
</div>
```

```javascript

    let modal = new Tinymodal('popup-example');
    document.getElementById('test-modal-link1').onclick = function() {
        modal.show();
        return false;
    }

```

Options
--------

List of options with default values:
```
{
    single: false,    // Close other modal windows when open new window
    esc: true,        // Close window on esc
    click: true,      // Close window on click in back
}
```
