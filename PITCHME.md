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
@[13-21](A brilliant way to define a component.)

---?gist=onetapbeyond/494e0fecaf0d6a2aa2acadfb8eb9d6e8&lang=scala&title=Scala GIST

@[23](You can even present code found within any GitHub GIST.)
@[41-53](GIST source code is beautifully rendered on any slide.)
@[57-62](And code-presenting works seamlessly for GIST too, both online and offline.)

---

## Template Help

- [Code Presenting](https://github.com/gitpitch/gitpitch/wiki/Code-Presenting)
  + [Repo Source](https://github.com/gitpitch/gitpitch/wiki/Code-Delimiter-Slides), [Static Blocks](https://github.com/gitpitch/gitpitch/wiki/Code-Slides), [GIST](https://github.com/gitpitch/gitpitch/wiki/GIST-Slides) 
- [Custom CSS Styling](https://github.com/gitpitch/gitpitch/wiki/Slideshow-Custom-CSS)
- [Slideshow Background Image](https://github.com/gitpitch/gitpitch/wiki/Background-Setting)
- [Slide-specific Background Images](https://github.com/gitpitch/gitpitch/wiki/Image-Slides#background)
- [Custom Logo](https://github.com/gitpitch/gitpitch/wiki/Logo-Setting), [TOC](https://github.com/gitpitch/gitpitch/wiki/Table-of-Contents), and [Footnotes](https://github.com/gitpitch/gitpitch/wiki/Footnote-Setting)

---

### Template Versions

- #### [Base Template  @fa[external-link gp-download]](https://gitpitch.com/gitpitch/templates/blue)
- #### [Code Maximized @fa[external-link gp-download]](https://gitpitch.com/gitpitch/templates/blue?p=codemax)
- #### [Speaker Notes @fa[external-link gp-download]](https://gitpitch.com/gitpitch/templates/blue?p=speaker)

---

### Questions?

<br>

@fa[twitter gp-contact](@gitpitch)

@fa[github gp-contact](gitpitch)

@fa[medium gp-contact](@gitpitch)

---?image=assets/image/gitpitch-audience.jpg

@title[Download this Template!]

### <span class="white">Get your presentation started!</span>
### [Download this template @fa[external-link gp-download]](https://gitpitch.com/template/download/blue)

