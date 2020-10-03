# Bootstrap HTML5 History Tabs
Bootstrap tabs that keep track of the history using the HTML5 History API

Requires jQuery and Bootstrap Tabs to work.

## How to use

Simply target the tabs tabs that you want to keep a history with and call the historyTabs plugin.

```javascript
$('a[data-toggle="tab"]').historyTabs();
```

This uses the default bootstrap implementation shown on their site. The links should be page links ('#link') in order for the value to be added to the URL properly. An example of this is below:

```html
<div role="tabpanel">
    <!-- Nav tabs -->
    <ul class="nav nav-tabs" role="tablist">
        <li role="presentation"><a href="#home" aria-controls="home" role="tab" data-toggle="tab">Home</a></li>
        <li role="presentation"><a href="#profile" aria-controls="profile" role="tab" data-toggle="tab">Profile</a></li>
        <li role="presentation"><a href="#messages" class="active" aria-controls="messages" role="tab" data-toggle="tab">Messages</a></li>
        <li role="presentation"><a href="#settings" aria-controls="settings" role="tab" data-toggle="tab">Settings</a></li>
    </ul>
    <!-- Tab panes -->
    <div class="tab-content">
        <div role="tabpanel" class="tab-pane" id="home">Home Tab</div>
        <div role="tabpanel" class="tab-pane" id="profile">Profile Tab</div>
        <div role="tabpanel" class="tab-pane active" id="messages">Messages Tab</div>
        <div role="tabpanel" class="tab-pane" id="settings">Settings Tab</div>
    </div>
</div>
```

When clicking on #settings link, you will notice the URL update to be baseurl/#settings. If you have an active tab set, then that tab will begin the history and will be added to the URL immediately. On the load of the page, it will use the hash value in the URL in order to load the correct tab. On back and forward, it will use the current history state in order to load the URL.
