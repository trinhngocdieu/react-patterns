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
- State hoisting |

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
const Greeting = (props, context) => {
  const style = {
    fontWeight: "bold",
    color: context.color,
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


@[0,2](ES6 feature)
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

### References

- #### [React Official Site  @fa[external-link gp-download]](https://gitpitch.com/gitpitch/templates/blue)
- #### [React Patterns @fa[external-link gp-download]](https://gitpitch.com/gitpitch/templates/blue?p=codemax)
- #### [Slide @fa[external-link gp-download]](https://gitpitch.com/gitpitch/templates/blue?p=speaker)

---

### Questions?

<br>

@fa[twitter gp-contact](@trinhngocdieu)


---?image=assets/image/gitpitch-audience.jpg

@title[Download this Template!]

### <span class="white">Get your presentation started!</span>
### [Download this template @fa[external-link gp-download]](https://gitpitch.com/template/download/blue)

