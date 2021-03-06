# react-list

This is a high performance list component and supports section feature.

## Concept:

### Visible Area: 
The visible area in the list, it's height equals listHeight.

### Render Area:
The area where to render items,it's height equals visible height plus buffer height (maybe both of top and bottom buffer area)

### Buffer Count:
The maximum count of buffer items to be rendered at top or bottom of Visible Area


## Intro:
This component is suitable for huge number of items, especially the total count of items is known.

The height of scroll bar will reflect the total count of items.

In order to ensure high performance, no matter how much items, it will eventually render the items which in the visible area and the buffer settings.

Thanks to React ensures that the minimum number of DOM operations are guaranteed during scrolling.

## Usage:
Without section feature:
- Feed "data" prop as an array of item data object.
- Implement "renderItem" method to responsible for rendering a item row.
- Feed "itemHeight" as either a fixed item height (number) or a function that returns the dynamic height of a item.

With section feature:
- Feed "enableSection" prop as true, and then feed "data" prop as an array of section data object.
- Implement "renderItem" method to responsible for rendering a item row.
- Implement "renderSectionHeader" method to responsible for rendering a section header row.
- Feed "itemHeight" as either a fixed item height (number) or a function that returns the dynamic height of a item.
- Feed "sectionHeaderHeight" as a fixed section header height.

> Note: It uses shallow compare as a performance optimization.
