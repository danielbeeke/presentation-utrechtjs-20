###  Templating
```
import Template from './templates/group-settings.html!text';

// Method inside Plugin
groupSubRoutes (group) {
    return [{
        path: '/groups/' + group.slug + '/settings',
        title: 'Settings',
        components: {
            main: {
                template: Template
                methods: {
                    saveSettings: function () {}
                },
            }
        },
    }];
}
```
