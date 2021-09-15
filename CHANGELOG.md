# Change Log

## [1.0.6] 2021-09-15 
### Improvements

- Bump Django Codebase to [v2.0.4](https://github.com/app-generator/boilerplate-code-django-dashboard/releases)
  - Codebase update
    - `assets` & `templates` moved to `apps` folder
    - `apps/base` renamed to `apps/home`

## [1.0.5] 2021-09-07
### Improvements & Fixes

- Bump Django Codebase to [v2.0.2](https://github.com/app-generator/boilerplate-code-django-dashboard/releases)
  - Dependencies update (all packages)
    - Use Django==3.2.6 (latest stable version)
  - Better Code formatting
  - Improved Files organization
  - Optimize imports
  - Docker Scripts Update 
- Fixes: 
  - Patch 500 Error when authenticated users access `admin` path (no slash at the end)
  - Patch [#16](https://github.com/app-generator/boilerplate-code-django-dashboard/issues/16): Minor issue in Docker 

## [1.0.4] 2021-06-30

- Update UI - Volt PRO v1.4.1
- Added scripts to recompile the SCSS files
    - `core/static/assets/` - gulpfile.js
    - `core/static/assets/` - package.json

## [1.0.3] 2021-06-15

- Correct 404 Links - UI Docs 

## [1.0.2] 2021-04-25
### Improvements

- Bump UI: Volt PRO v1.3.1
- UI: [Jinja Volt PRO](https://github.com/app-generator/jinja-template-volt-pro/releases) v1.0.3

## [1.0.1] 2021-01-20

- UI: [Jinja Volt PRO](https://github.com/app-generator/jinja-template-volt-pro/releases) v1.0.2
- Volt PRO v1.2.0
- Codebase - [Django Dashboard](https://github.com/app-generator/boilerplate-code-django-dashboard/releases) v1.0.4

## [1.0.0] 2020-02-07
### Initial Release
