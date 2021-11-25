# OpenProject Plugin CI

This action works with your custom plugin to automate testing and linting.

## What Works

- Angular unit testing
- Rspec unit tests

## Work In Progress

- Linting
- Rspec features tests

## Usage

In your workflow file, add a step with the following:

```yml
uses: bitcrowd/openproject-plugin_test_action@v1
with:
  # Name of the plugin to test as listed in the Gemfile.plugins
  pluginName: ""
  # Version of OpenProject to test against. Must be a branch or tag name from https://github.com/opf/openproject.
  # Default: v12.0.2
  openprojectVersion: ""
  # The test steps to use. Must be given in the order outlined in the default value but you can leave out some tests if you want.
  # Default: run-angular-unit run-rspec-unit run-rspec-features run-frontend-lint
  testSteps: ""
```
