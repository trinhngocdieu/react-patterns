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
- JSX Spread Attributes |
- Destructuring arguments |
- Conditional Rendering |
- Function as children |
- Container component |
- State hoisting |
- Layout component |


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


---

@title[JSX Spread Attributes]

<p><span class="slide-title">JSX Spread Attributes</span></p>

```javascript
<main className="main" role="main">{children}</main>

<main {...{className: "main", role: "main", children}} />

```

@[0,1](Props written as attributes)
@[3,4](Props "spread" from object)


---


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

