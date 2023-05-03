# EmberJS Tests

## Pause tests

Pauses the current test to interact with the view. It allows you to inspect the state of your application at any point.

Example (**ember-qunit**):

```
import { setupRenderingTest } from 'ember-qunit';
import { render, click, pauseTest } from '@ember/test-helpers';

module('Integration | Component | awesome-component', function (hooks) {
  setupRenderingTest(hooks);

  test('does something awesome', async function (assert) {
    await render(hbs`<AwesomeComponent />`);

    // added here to visualize / interact with the DOM prior
    // to the interaction below
    await pauseTest();
  });
});
```

Run:

```
ember t -s -m "Integration | Component | awesome-component"
```

### References

- Ember Test helpers - [https://github.com/emberjs/ember-test-helpers/blob/master/API.md](https://github.com/emberjs/ember-test-helpers/blob/master/API.md)
