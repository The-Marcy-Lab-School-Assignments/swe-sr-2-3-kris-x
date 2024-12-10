# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

What are the main differences between Flexbox and Grid layouts? Describe scenarios where each layout system would be more suitable.

### Response 1
Some of the main differences between Flexbox and Grid layouts are that Grid Layouts are more suitable for complex and structured layouts whereas Flexbox is more ideal for simpler layouts. Secondly, Flexbox is more focused on aligning items along a single axis. Grid layouts are better for controlling the alignment and positioning of elements inside a grid as a whole. Lastly, another difference between Flexbox and Grid layouts is that items align based on content flow like the wrapping of the content, direction, or justifying the content. Here's a scenario for Flexbox: Let's say you're inside of your CSS file and you have a navigation menu that is evenly spaced. You can use Flexbox when you need to arrange elements along a single axis, you can use Flexbox to evenly distribute space between items. A scenario for Grid: Let's say you have a web page layout with a header, footer, sidebar, and content area defined within a 12-column grid system. In this case, you would use Grid layouts because you need a more structured layout with explicit rows and columns.

## Prompt 2

What is the difference between `justify-content` and `align-items` in Flexbox? How does each property control the positioning of flex items within the container?

```
Justify-content aligns items along the main axis(horizontally), controlling space distribution within a container. In contrast, align-items align items along the cross-axis (vertically), managing how items are placed relative to each other inside a container.

```

## Prompt 3

Describe the difference between `grid-template-areas` and `grid-template-columns`/`grid-template-rows`. When might you prefer one approach over the other?

### Response 3
`grid-template-areas` defines the layout structure using named areas on a grid pattern. `grid-template-areas` offers a high-level, semantic representation of the grid layout, making it easier to understand the design. `grid-template-columns` and `grid-template-rows` on the other hand provides precise control over the size and spacing of the grid lines but doesn’t directly define the relationship between grid items and their positions. `grid-template-columns` and  `grid-template-rows` also use values like px, fr, %, or auto to set widths and heights of rows/columns. You would use `grid-template-areas` when you want a visual representation of the layout structure in the CSS file and when you want to place and rearrange major sections easily without changing the row/column sizes. In cases where you need detailed control over the dimensions of rows and columns or if the layout doesn’t require named areas, defining rows and columns directly, you would use `grid-template-columns` and `grid-template-rows`.

## Prompt 4

Explain the `min-width` and `max-width` keywords in media queries. How do they help create responsive breakpoints for different screen sizes?

```
Min-width is used if the screen/window is equal to or more than the given pixels, then the code in the query will trigger, while max-width is if the screen/window is equal to or less than the given pixels, then the code in the query will trigger. They help create responsive breakpoints for different screen sizes by making specific elements for each. You can make and add styles that only apply to the screen sizes equal to the given pixels. It adds more customization and design, giving you more control over how you want your website to look on certain screens.

```

## Prompt 5

Imagine you are teaching a brief lesson on **mobile first design**. Your lesson should include the following information:

- An explanation of mobile first design and a few of the benefits of this approach
- A CSS code example demonstrating how to use media queries to adjust the layout of a container from mobile to desktop with either Flexbox or Grid (choose one).
- An explanation of the code example.

### Response 5
Mobile-first design is a web development approach that begins with designing for mobile devices and then progressively enhances the layout and features for larger screens. The idea is to prioritize essential content and functionality on smaller screens, where space and resources are limited, and scale up for desktop users. Some of the benefits of Mobile First Design is by prioritizing lightweight and essential content, mobile pages tend to load faster, this is a benefit because it improves user experience. Mobile users expect quick load times, often abandoning pages that take more than a few seconds to load. Faster pages keep users engaged, likewise, convenience is another benefit, mobile users are often on the go and need quick access to information, making fast-loading pages essential. Here's a CSS code example demonstrating how to use media queries to adjust the layout of a container from mobile to desktop with Grid.

```CSS

.container {
  display: grid;
  grid-template-columns: 1fr; 
  gap: 16px; 
  padding: 16px; 
}

min-width: 700px {
  .container {
    grid-template-columns: 1fr 2fr; 
    gap: 24px; 
  }
}
```
Here's an explanation of the CSS, The .container is defined as a grid with grid-template-columns: 1fr, creating a single column. gap: 16px provides consistent spacing between items. These styles are the default, ensuring a simple, functional layout for smaller screens. The min-width: 768px query targets devices with a viewport width of 768px or larger. Inside the query, grid-template-columns: 1fr 2fr creates two columns, with the second column twice as wide as the first, gap: 24px increases the spacing to accommodate the larger screen size.