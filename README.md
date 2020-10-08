# Reactstrap confirm 


An easy to use promise based confirm dialog for reactstrap.

The objective of this modification is to offer developers a property to avoid user errors when clicking outside the elements or buttons


## Installation

Simply use npm

```bash
npm i --save reactstrap-confirm-by-jdionicio
```

You can use yarn as well

```bash
yarn add reactstrap-confirm-by-jdionicio
```

## Dependencies

You must manually install react, react-dom and reactstrap in your project in order for this module to work correctly.

## Usage

Simply, import the module and call it as a function anywhere in your code.

```javascript
import confirm from "reactstrap-confirm-by-jdionicio";

// ...code

let result = await confirm(); //will display a confirmation dialog with default settings

console.log(result); //if the user confirmed, the result value will be true, false otherwhise
```

You can also pass options to the confirm function:

```javascript
confirm({
    title: (
        <>
            Content can have <strong>JSX</strong>!
        </>
    ),
    message: "This is a custom message",
    confirmText: "Custom confirm message",
    confirmColor: "primary",
    cancelColor: "link text-danger"
});
```

The above example will render a customized dialog.

### Available options

| Option           | Effect                                                                                                        | Default value |
| ---------------- | ------------------------------------------------------------------------------------------------------------- | ------------- |
| message          | Sets the message body of the confirmation dialog                                                              | Are you sure? |
| title            | Sets the title of the dialog window                                                                           | Warning!      |
| confirmText      | Sets the text of the confirm button                                                                           | Ok            |
| cancelText       | Sets the text of the cancel button                                                                            | Cancel        |
| confirmColor     | Sets the color class of the confirm button (see reactstrap docs)                                              | primary       |
| cancelColor      | Sets the color class of the cancel button (see reactstrap docs)                                               | _empty_       |
| size             | Sets the size property for the modal component (see reactstrap docs)                                          | _empty_       |
| buttonsComponent | Can receive a component for rendering the buttons. The component will receive the onClose function as a prop. | _empty_       |
| closedforContent | Avoid closing the modal when clicking on the div that contains it. | true       |
