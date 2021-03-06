---
id: migrating
title: Migrating
---

## Migrating from formik-material-ui 1.0.0

### Standard Components

### Changes

- `type=checkbox` recommended for Switches and Checkboxes - See [here](https://jaredpalmer.com/formik/docs/migrating-v2#checkboxes-and-select-multiple)

#### Before

```jsx
import { Field } from 'formik';
import { Checkbox, Switch } from 'formik-material-ui';

<Field name="checkbox" component={Checkbox} />;
<Field name="switch" component={Switch} />;
```

- Rename fieldToTextField to useFieldToTextField
- Add `import {useField} from 'formik'` if you need access to field helpers
- Add `import {useFormik} from 'formik'` if you need access to form helpers

#### After

```jsx
import { Field } from 'formik';
import { Checkbox, Switch } from 'formik-material-ui';

<Field name="checkbox" type="checkbox" component={Checkbox} />;
<Field name="switch" type="checkbox" component={Switch} />;
```
