# Vizstack Blog
Welcome to our blog! This is where we share exciting updates and milestones on our journey that is building Vizstack.

## Updates
[Week 11/17](WEEK-11-17.md) (Latest) - Finished building Pytorch neural network visualizer, improved graph appearance!

[Week 11/10](WEEK-11-10.md) - Improve structure visualization of complex neural networks!

[Week 11/03](WEEK-11-03.md) - Implement orthogonal edge routing and improved force model for RNNs!

[Week 10/27](WEEK-10-27.md) - Redesign `DagLayout` lifecycles and better rendering for neural networks!

[Week 10/20](WEEK-10-20.md) - Improve `vz-pytorch` computation graph visualizer and `core` fragments!

[Week 10/13](WEEK-10-13.md) - Finalize `nodal` landing page content & repo, prototype `vz-pytorch` computation graph visualizer!

[Week 10/06](WEEK-10-06.md) - Published `nodal` landing page v2 with interactive demo/code generation, plus other new features!

[Week 09/29](WEEK-09-29.md) - Built `nodal` landing page v1, fully integrate shapes, and improve graph layout!

[Week 09/22](WEEK-09-22.md) - Redesigned core aesthetics, improved `nodal` library, and shapes, shapes, shapes!

[Week 09/15](WEEK-09-15.md) - Added graph layout features, fine-tuned force models, integrated with `core` library!

[Week 09/08](WEEK-09-08.md) - Designed/implemented extremely modular & extensible `nodal` graph layout library!

[Week 09/01](WEEK-09-01.md) - Created MVP for `vz-logger` (Javascript + Python), optimized design for complex layouts!

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
