# Q HHVM Test Runner

This test runner was created during Hack Week Spring 2019. The goal was to minimize errors in executing tests on full-stack environments due to misspellings and or forgotten command flags. The test runner allows for the user to execute all tests within a test file or a single test (when the test name is highlighted) using a series of keypresses. 

### Instructions to Use
1. Download the package 
2. In VS Code, press Command + Shift + P to pull up the Command Palette.
3. Type `Install from VSIX` and select
4. Select the downloaded package

```
Commands are the following when in a Hack test file.

To run a full test file:
- Command + Control + T runs with --no-watch (does not watch for changes in test file)
  - Equivalent to yarn fs-ctl test-hhvm QSetTest --no-watch
- Command + Control + Y (watches for changes in test file)
  - Equivalent to yarn fs-ctl test-hhvm QSetTest

To run an individual test, highlight the name:
- Command + Control + T runs with --no-watch (does not watch for changes in test file)
  - Equivalent to yarn fs-ctl test-hhvm QSetTest::testCannotMakeDmcaPrivacyLockedSetsPublic --no-watch
- Command + Control + Y (watches for changes in test file)
  - Equivalent to yarn fs-ctl test-hhvm QSetTest::testCannotMakeDmcaPrivacyLockedSetsPublic
```

### Instructions to Generate VSIX File
For any new features or modifications, be sure to update the version in `package.json` as this is used to generate the file name.

1. Ensure `vsce` is installed (`npm i -g vsce`)
2. Run `vsce package` and follow prompts

---

### About

This extension inspired by [terminal-command-keys](https://github.com/petekinnecom/terminal-command-keys).