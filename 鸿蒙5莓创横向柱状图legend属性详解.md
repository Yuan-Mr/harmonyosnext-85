### Hello and welcome back to our special session on HarmonyOS 5 Berry Creative chart components. In this episode, we'll explore the detailed usage of the **legend** property in combination charts. The legend is a crucial component that helps users identify data series represented by different colors or shapes. Let's dive into each legend property and its applications.  


### 1. `show` - Toggle Legend Visibility  
**Function**: Controls whether the legend is displayed.  
**Type**: Boolean  
**Default**: `true`  
**Options**: `true` | `false`  
**Scenario**: Hide the legend when unnecessary.  

**Example**:  
```json
legend: {
  show: false  // Hide the legend
}
```  


### 2. `orient` - Legend Orientation  
**Function**: Sets the layout direction of legend items.  
**Type**: String  
**Default**: `'horizontal'`  
**Options**: `'horizontal'` | `'vertical'`  
**Scenario**: Use `vertical` for long legend lists.  

**Example**:  
```json
legend: {
  orient: 'vertical'  // Vertical layout
}
```  


### 3. `left`/`right`/`top`/`bottom` - Legend Position  
**Function**: Positions the legend within the chart.  
**Type**: String | Number  
**Default**: `'auto'`  
**Options**: `'auto'`, percentage (e.g., `'10%'`), or pixel value (e.g., `20`).  
**Scenario**: Precise positioning relative to the chart container.  

**Example**:  
```json
legend: {
  left: '10%',   // 10% from left
  top: 20,       // 20px from top
  right: 'auto', // Auto-position right
  bottom: '5%'   // 5% from bottom
}
```  


### 4. `icon` - Legend Item Shape  
**Function**: Sets the icon shape for legend items.  
**Type**: String  
**Default**: `'roundRect'`  
**Options**: `'rect'` | `'circle'` | `'roundRect'`  
**Scenario**: Match icon style to chart design.  

**Example**:  
```json
legend: {
  icon: 'circle'  // Use circular icons
}
```  


### 5. `iconRadian` - Icon Corner Radius  
**Function**: Sets the corner radius for rounded rectangles (only for `icon: 'roundRect'`).  
**Type**: Number  
**Default**: 2  
**Scenario**: Adjust corner smoothness.  

**Example**:  
```json
legend: {
  icon: 'roundRect',
  iconRadian: 5  // Larger rounded corners
}
```  


### 6. `itemGap` - Spacing Between Items  
**Function**: Sets the gap between legend items.  
**Type**: Number  
**Default**: 10  
**Scenario**: Control item density.  

**Example**:  
```json
legend: {
  itemGap: 20  // Increased spacing
}
```  


### 7. `itemTextGap` - Icon-Text Spacing  
**Function**: Sets the gap between the icon and text.  
**Type**: Number  
**Default**: 5  
**Scenario**: Improve readability.  

**Example**:  
```json
legend: {
  itemTextGap: 8  // Larger gap
}
```  


### 8. `align` - Icon-Text Alignment  
**Function**: Aligns icons and text in vertical layouts.  
**Type**: String  
**Default**: `'auto'`  
**Options**: `'auto'` | `'left'` | `'right'`  
**Scenario**: Control alignment in vertical legends.  

**Example**:  
```json
legend: {
  orient: 'vertical',
  align: 'right'  // Right-align items
}
```  


### 9. `itemWidth`/`itemHeight` - Icon Size  
**Function**: Sets icon dimensions.  
**Type**: Number  
**Default**: `itemWidth=8`, `itemHeight=8`  
**Scenario**: Resize icons for better visibility.  

**Example**:  
```json
legend: {
  itemWidth: 12,
  itemHeight: 12  // Larger icons
}
```  


### 10. `selectAble` - Item Selection  
**Function**: Enables/disables clicking legend items to toggle series visibility.  
**Type**: Boolean  
**Default**: `true`  
**Scenario**: Disable interaction when needed.  

**Example**:  
```json
legend: {
  selectAble: false  // Disable selection
}
```  


### 11. `data` - Legend Content  
**Function**: Defines legend items.  
**Type**: Array  
**Default**: `[]`  
**Scenario**: Customize legend labels.  

**Example**:  
```json
legend: {
  data: ['Q1', 'Q2', 'Q3', 'Q4']  // Custom labels
}
```  


### 12. `textStyle` - Text Appearance  
**Function**: Configures legend text style.  

#### Sub-properties:  
- **`fontFamily`**: Font family (default: `'sans-serif'`).  
- **`fontWeight`**: Font weight (default: `'normal'`).  
- **`fontSize`**: Font size (default: `30`).  
- **`color`**: Text color (default: `'#333'`).  
- **`formatter`**: Text formatting (default: `null`).  

**Example**:  
```json
legend: {
  textStyle: {
    fontFamily: 'Arial',
    fontWeight: 'bold',
    fontSize: 14,
    color: '#666',
    formatter: '{value} Items'  // Append unit
  }
}
```  


### 13. `iconStyle` - Icon Appearance  
**Function**: Customizes legend icon style.  
**Type**: Object  
**Default**: `{}`  

**Example**:  
```json
legend: {
  iconStyle: {
    color: '#FF0000',      // Red icons
    borderColor: '#000',   // Black border
    borderWidth: 1         // 1px border
  }
}
```  


### 14. `textUnselectedStyle` - Unselected Text Style  
**Function**: Configures text style for unselected items.  

#### Sub-properties:  
- **`fontFamily`**: Font family (default: `'sans-serif'`).  
- **`fontSize`**: Font size (default: `30`).  
- **`color`**: Text color (default: `'#999'`).  

**Example**:  
```json
legend: {
  textUnselectedStyle: {
    fontFamily: 'Arial',
    fontSize: 12,
    color: '#CCC'  // Lighter color
  }
}
```  


### 15. `iconUnselectedStyle` - Unselected Icon Style  
**Function**: Customizes icon style for unselected items.  
**Type**: Object  
**Default**: `{color: '#999'}`  

**Example**:  
```json
legend: {
  iconUnselectedStyle: {
    color: '#DDD',   // Lighter color
    opacity: 0.5     // Semi-transparent
  }
}
```  


### 16. `rLevel` - Render Priority  
**Function**: Sets rendering order (z-index).  
**Type**: Number  
**Default**: 20  
**Scenario**: Control layering with other components.  

**Example**:  
```json
legend: {
  rLevel: 30  // Higher priority
}
```  


### 17. `animationCurve` - Animation Easing  
**Function**: Sets animation curve for state changes.  
**Type**: String  
**Default**: `'easeOutCubic'`  
**Scenario**: Customize animation feel.  

**Example**:  
```json
legend: {
  animationCurve: 'linear'  // Linear animation
}
```  


### 18. `animationFrame` - Animation Duration  
**Function**: Sets animation duration (frames).  
**Type**: Number  
**Default**: 0 (no animation)  
**Scenario**: Control animation smoothness.  

**Example**:  
```json
legend: {
  animationFrame: 30  // 30-frame animation
}
```  


### Practical Example  
Here's a complete configuration demonstrating multiple legend properties:  

```json
{
  legend: {
    show: true,
    orient: 'horizontal',
    left: 'center',
    top: '5%',
    icon: 'roundRect',
    iconRadian: 4,
    itemGap: 15,
    itemTextGap: 8,
    itemWidth: 12,
    itemHeight: 12,
    selectAble: true,
    data: ['Q1 Sales', 'Q2 Sales', 'Q3 Sales', 'Q4 Sales'],
    textStyle: {
      fontFamily: 'Microsoft YaHei',
      fontWeight: 'normal',
      fontSize: 12,
      color: '#333',
      formatter: '{value} Sales'
    },
    iconStyle: {
      color: '#FFF',
      borderColor: '#666',
      borderWidth: 1
    },
    textUnselectedStyle: {
      color: '#AAA',
      fontSize: 11
    },
    iconUnselectedStyle: {
      color: '#EEE',
      opacity: 0.7
    },
    animationCurve: 'easeOutQuad',
    animationFrame: 20
  },
  // Other chart configurations...
}
```  

This setup creates a horizontally centered legend with rounded rectangles, custom text formatting, and smooth animations.  


### Conclusion  
That wraps up our guide to the `legend` property in Berry Creative charts! Use these properties to create intuitive and visually appealing legends. If you have questions, leave them in the comments. Happy coding! 📊
