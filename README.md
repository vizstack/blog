# Vizstack Blog
Welcome to our blog! This is where we share exciting updates and milestones on our journey that is building Vizstack.

## Updates
[Week 09/01](WEEK-09-01.md) - Created MVP for vz-logger (Javascript + Python), optimized design for complex layouts!

## What is Vizstack?
> A programming environment that makes code and data structures easier to think about by rendering beautiful, interactive visualizations.

![Vizstack Structure](https://github.com/vizstack/blog/blob/master/img/vizstack-structure.png)

Here's a question for you: would you rather try to figure out how Vizstack works only by going through our GitHub code, or would you also like to consult the above diagram for reference? (For those that answered the former, have fun: https://github.com/vizstack/vizstack ... we'll wait XD).

Chances are, if you're like many programmers, trying to understand how a complex codebase works without a conceptual/visual map is an exercise in confusion and misery. Of course, diagrams by themselves aren't enough to convey everything, but just looking at the code doesn't seem right either. We need a way to combine the best of both worlds in order to reinvent the way we read, write, and debug code.

Vizstack's mission is to do just that, and we're tackling it in an iterative and progressive fashion, rather than building a completely new, monolithic application or visual programming language.

- **Core**: At the base layer, Vizstack provides declarative libraries (in multiple languages) to build complex, beautiful, interactive, data-driven visualizations. Our design philosophy is that, just like in LaTeX or Markdown, users should focus on their content and leave the aesthetic layout and tweaking to the machine. We are working towards a "grammar of software graphics", so that developers will be able to quickly and flexibly integrate visualization into their work. For instance, using the Typescript bindings you could write
```jsx
<Viewer view={
    Sequence([
        Text("Johnny Appleseed", 'heading'),
        Text("Joined on 9/1/2018", 'body', 'less'),
        KeyValue([
            [Text("status"), Token("active", 'green')],
            [Text("employeeId"), Text("12345678")],
            [Text("dateOfBirth"), Flow(Text('Oct'), Text('22'), Text('1986'))],
            [Text("pastJobs"), Sequence([
                Text("Software Engineer"), Text("UX Designer"), Text("AI Researcher")
            ])]
        ], { showLabels: false })
    ], { orientation: 'vertical', showLabels: false })
} />
```
to generate the following visualization that responds to mouse and keyboard interactions:
<img src="https://github.com/vizstack/blog/blob/master/img/core-example.png" width="440">

- **Apps**: At a higher level, developers can use `@vizstack/core` to build more complex, domain-specific applications. One example of this is `vz-logger`, which is a multi-platform logger that uses the core bindings to translate language-specific data structures into visualizations that can be displayed in a web-based dashboard.

**We're still in early alpha stage: stay tuned for more details and updates!**
