# reactn-crud-ui-antd

[Demo](http://reactn-crud.surge.sh/)

> Antd design Controller components for [reactn-crud](https://github.com/gengue/reactn-crud)
[![NPM](https://img.shields.io/npm/v/reactn-crud-ui-antd.svg)](https://www.npmjs.com/package/reactn-crud-ui-antd) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
npm install --save reactn-crud-ui-antd
```

## Usage

```jsx
import React from 'react'
import { ListController, ShowController,FormController } from 'reactn-crud-ui-antd';

function UserList(props) {
  const columns = [
    { title: 'Email', dataIndex: 'email', primary: true },
    { title: 'First Name', dataIndex: 'first_name', sorter: true },
    { title: 'Last Name', dataIndex: 'last_name', sorter: true },
  ];
  return (
    <ListController {...props} resource="users" columns={columns} />
  );
}

function UserShow(props) {
  const fields = [
    { dataIndex: 'email', title: 'Email' },
    {
      dataIndex: 'name',
      title: 'Full name',
      render: record => `${record.first_name} ${record.last_name}`,
    },
  ];
  return <ShowController {...props} fields={fields} resource="users" />;
}

function UserForm(props) {
  return (
    <FormController {...props} resource="users">
      <Input source="email" label="Email" type="email" required />
      <Input source="first_name" label="First Name" required />
      <Input source="last_name" label="Last Name" required />
    </FormController>
  );
}
```

## API

...IN PROGRESS

## TODO

* Add unit tests
* Improve documentation, add API section

## License

[MIT](LICENSE.md) © [Genesis Guerrero](https://github.com/gengue)
