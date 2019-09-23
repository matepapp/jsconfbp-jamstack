# JSConfBP JAMStack Workshop

During the workshop we're going to build a basic company e-commerce store where you and your fellow coworkers can buy cool SWAGs.

## Requirements

- Git
- Github account
- Editor of your choice
- Node.js (minimum v8)
- npm or yarn

To make communication and file sharing seamless we're using a Slack workspace. [You can join the workspace here.](https://join.slack.com/t/jsconfbp-jamstack/shared_invite/enQtNzY1OTIyNjIxMTI2LTg4Y2FlNTEzMDFhOTE2Yzg1ZjlhMmM2YWZiMWYxNjNjM2VkMjNlOTIyZTkzOWJkOTEwOWJkNWQyMTc0ZmRiMWQ)

If you have a question or you're stucked with something, feel free to ask our mentors or post it to Slack's **#help** channel.

## Part 1

### Tasks

start from branch: `41-cart`

#### Dispatch actions

1. Check action types `src/store/types`
2. find all alert() in the project and dispatch actions instead

Here is an example for the INCREMENT_QUANTITY action payload

```js
payload: {
    slug: '',
    name: '',
    price: 0,
}
```

Here is an example for the DECREASE_QUANTITY action payload

```js
payload: {
  slug: ''
}
```

## Part 2

### Tasks

#### Create database

1. Install the Netlify command-line tool `npm i netlify-cli -g`
2. Add the FaunaDB Add-on for Netlify `netlify addons:create fauna`
3. Authenticate the Add-on `netlify addons:auth fauna`

#### Mutate the state in the orders reducer

1. start your lambda function and the gatsby development server with `netlify dev`
2. after `LOAD_ORDER_HISTORY_SUCCESS` action you have to populate the state with the payload
3. after `CHECKOUT_SUCCESS` action you have to add the new item to the state
4. create a new dynamic route where you can list your last order, you can use the `Orders` component.
