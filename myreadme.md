# Learning Goals
1. Understand the use cases for programmatic navigation
2. Use the useHistory hook to perform programmatic navigation
3. Use the <Redirect> component to perform programmatic navigation

**useHistory hook**

By calling `history.push()`, we can effectively navigate the user to a new page
in response to **any** event in our application, not just when the user clicks a
link!

**Redirect component**

This component is particularly useful in cases where you need to handle some
conditional rendering. For example:

```jsx
function Home({ isSignedIn }) {
  // if the user isn't signed in, redirect them to the login page
  if (!isSignedIn) return <Redirect to="/login" />;

  // otherwise, return the home page
  return (
    <div>
      <h1>Home!</h1>
    </div>
  );
}
```