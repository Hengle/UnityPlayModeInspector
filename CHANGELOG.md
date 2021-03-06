# Changelog
All notable changes to this package are documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).
 
## [1.1.0] - 2020-07-18
### Added
 - Functionality to override the default display name shown in the PlayMode Inspector item header. Use the "displayName" property found in the PlayModeInspectorMethod attribute for this.
 - Functionality to expand/collapse an item by clicking anywhere in the header, rather than on the toggle only.

### Fixed
 - Window icon barely visible with Professional Editor Theme (Issue #1).
 - Clicking the "Add PlayMode Inspector" button to create a new window, displays the current selected object now, rather than an empty window.
 - Do not call PlayMode Inspector method on prefabs in the project. Call the method only, when the object is located in a scene. This is necessary, because all the Awake/Start/OnEnable/etc methods are only called on Components in a scene. And if we would call the PlayMode Inspector method on a prefab in the project, it most likely is in an undefined state.
 - Do not call PlayMode Inspector method on inactive components. This is necessary, because the Component perhaps hasn't initialized and thus is in an undefined state.
 - Do not call PlayMode Inspector method on Components in the prefab stage, because all the Awake/Start/OnEnable/etc methods are only called on Components in a scene. And if we would call the PlayMode Inspector method on a prefab in the project, it most likely is in an undefined state.

## [1.0.0] - 2020-05-31
 - First public release
