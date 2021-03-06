# React Patterns

### @trinhngocdieu

---

## Me!

<br>

@fa[arrows gp-tip](Front-end Developer @ Zalo)

@fa[microphone gp-tip](Speak JS, ReactJS, NodeJS)

---

## Content

- Stateless function |
- Destructuring arguments |
- JSX Spread Attributes |
- Conditional Rendering |
- Render callback |
- Layout component |
- Container component |
---

@title[Stateless Function]

<p><span class="slide-title">Stateless Function</span></p>

```javascript
class Greeting extends React.Component {
  constructor() {
    super();
  }
  
  componentDidMount() {}
  
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}

// A brilliant way to define a component.
// Don’t hold state; they’re just functions.
const Greeting = (props) => {
  const style = {
    fontWeight: "bold",
    color: "blue",
  }

  return <div style={style}>{props.name}</div>
}
```

@[0,11](Normal way to define a component.)
@[13-22](Example: UserInfo, Flag Selector, ...)

---
@title[Destructuring Arguments]

<p><span class="slide-title">Destructuring Arguments</span></p>

```javascript
const Greeting = props => <div>Hi {props.name}!</div>
const Greeting = ({ name }) => <div>Hi {name}!</div>

const Greeting = ({ name, ...props }) =>
  <div>Hi {name}!</div>
```


@[0-2](ES6 feature)
@[3-5](Using REST PARAMETER to collect all the remaining props)

---

@title[JSX Spread Attributes]

<p><span class="slide-title">JSX Spread Attributes</span></p>

```javascript
<main className="main" role="main">{children}</main>
<main {...{className: "main", role: "main", children}} />

const FancyDiv = props =>
  <div className="fancy" {...props} />
  
// Example
<FancyDiv data-id="my-fancy-div">So Fancy</FancyDiv>
// output: <div className="fancy" data-id="my-fancy-div">So Fancy</div>

const FancyDiv = props =>
  <div {...props} className="fancy" />
  
const FancyDiv = ({ className, ...props }) =>
  <div
    className={["fancy", className].join(' ')}
    {...props}
  />
```

@[0-2](Props "spread" from object)
@[3-8](Forward to another component)
@[10-13](`className` clobbers your `className`)
@[14-18](separate className and spread the remains)

---
@title[Conditional Rendering]

<p><span class="slide-title">Conditional Rendering</span></p>

```javascript
// if
{condition && <span>Rendered when `truthy`</span> }

// unless
{condition || <span>Rendered when `falsey`</span> }

// if -- else 
{condition
  ? <span>Rendered when `truthy`</span>
  : <span>Rendered when `falsey`</span>
}
```
@[0-10](Our JSX Structure will be clearer)

---

@title[Render Callback]

<p><span class="slide-title">Render Callback</span></p>

```javascript
const Width = ({ children }) => children(500)

<Width>
  {width => <div>window is {width}</div>}
</Width>

// output
<div>window is 500</div>

<Width>
  {width =>
    width > 600
      ? <div>min-width requirement met!</div>
      : null
  }
</Width>

// Rendering our app depends on with 
class WindowWidth extends React.Component {
  constructor() {
    super()
    this.state = { width: 0 }
  }

  componentDidMount() {
    this.setState(
      {width: window.innerWidth},
      window.addEventListener(
        "resize",
        ({ target }) =>
          this.setState({width: target.innerWidth})
      )
    )
  }

  render() {
    return this.props.children(this.state.width)
  }
}

```
@[0-1](children as FUNCTION, with argument 500)
@[2-8](give it a FUNCTION as children)
@[9-16](make rendering decision)
@[18-40](example)


---

@title[Layout Component]

<p><span class="slide-title">Layout Component</span></p>

```javascript
<HorizontalSplit
  leftSide={<SomeSmartComponent />}
  rightSide={<AnotherSmartComponent />}
/>

class HorizontalSplit extends React.Component {
  shouldComponentUpdate() {
    return false
  }

  render() {
    <FlexContainer>
      <div>{this.props.leftSide}</div>
      <div>{this.props.rightSide}</div>
    </FlexContainer>
  }
}
```

---

@title[Container Component]

<p><span class="slide-title">Container Component</span></p>

```javascript
const CommentList = ({ comments }) =>
  <ul>
    {comments.map(comment =>
      <li>{comment.body}-{comment.author}</li>
    )}
  </ul>
  
class CommentListContainer extends React.Component {
  constructor() {
    super()
    this.state = { comments: [] }
  }

  componentDidMount() {
    $.ajax({
      url: "/my-comments.json",
      dataType: 'json',
      success: comments =>
        this.setState({comments: comments});
    })
  }

  render() {
    return <CommentList comments={this.state.comments} />
  }
}
```
@[0-6](// Reusable Components)
@[7-25](// Fetching data, rendering CommentList)

---

### References

- #### [React Site @fa[external-link gp-download]](https://reactjs.org/)
- #### [React Patterns @fa[external-link gp-download]](https://egghead.io/courses/advanced-react-component-patterns)
- #### [My Site @fa[external-link gp-download]](https://trinhngocdieu.com)

---

### Questions?

<br>

@fa[twitter gp-contact](@trinhngocdieu)


---?image=assets/image/gitpitch-audience.jpg

@title[Thank You!]

### <span class="white">Thanks for your attention!</span>
### [Have a nice weekend @fa[external-link gp-download]](https://gitpitch.com/template/download/blue)

