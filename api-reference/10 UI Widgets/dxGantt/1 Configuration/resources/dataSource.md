---
id: dxGantt.Options.resources.dataSource
type: Array<Object> | DataSource | DataSource_Options
default: null
---
---
##### shortDescription
Binds the widget to the data source, which contains resources.

---
---

##### jQuery

    <!-- tab: index.js -->
    $(function() {
        $("#gantt").dxGantt({
            resources: {
                dataSource: resources
            },
            //...
        });
    });
    <!-- tab: data.js -->
    var resources = [{
        'id': 1,
        'text': 'Management'
    }, 
    // ...
    ];    

##### Angular

    <!-- tab: app.component.ts -->
    import { DxGanttModule } from 'devextreme-angular';
    import { Service, Task, Dependency, Resource, ResourceAssignment } from './app.service';
    // ...
    export class AppComponent {
        resources: Resource[];		
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxGanttModule
        ],
        // ...
    })
    <!-- tab: app.component.html -->
    <dx-gantt ... 
        <dxo-resources [dataSource]="resources"></dxo-resources>
		// ...
    </dx-gantt>
    <!-- tab: app.service.ts -->
    let resources: Resource[] = [{
        'id': 1,
        'text': 'Management'
    },
    // ...   
    ]; 
     

##### Vue

    <!-- tab: App.vue -->
    <template>
        <DxGantt ...
            <DxResources :data-source="resourcesDataSource"/>
			// ...
        </DxGantt>
    </template>
    <script>
        import {
            DxGantt,
            DxResources,
			// ...
        } from 'devextreme-vue/gantt';

        import {
            resources,
			// ...
        } from './data.js';

        export default {
            components: {
                DxGantt,
                DxResources,
				// ...
            },
            data() {
                return {
                resources,
				// ...
                };
            },
            computed: {
                resourcesDataSource() { return resources; },
				// ...
            }
        };
    </script>
    <!-- tab: data.js -->
    export const resources = [{
        'id': 1,
        'text': 'Management'
    },
    // ...
    ];	
	
##### React

    <!-- tab: App.js -->
    import React from 'react';
    import Gantt, { Tasks, Dependencies, Resources, ResourceAssignments, Column, Editing } from 'devextreme-react/gantt';
    import { tasks, dependencies, resources, resourceAssignments } from './data.js';

    class App extends React.Component {
        render() {
            return (
            <Gantt ...       
                <Resources dataSource={resources} />
				// ...
            </Gantt>
            );
        }
    }
    export default App;
    <!-- tab: data.js -->
    export const resources = [{
        'id': 1,
        'text': 'Management'
    },
    // ...
    ];

---
