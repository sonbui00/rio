---
title: 'Navigation'
language: 'en'
---

Rio allows to choose navigation between the following options:

### CollapsedTab

The <span class="keyword">CollapsedTab</span> is Rio terminal default navigation mode for Linux, BSD and Windows.

Note: The example below is using Dracula color scheme instead of Rio default colors.

<img src="https://miro.medium.com/v2/resize:fit:1400/format:webp/1*gMLWcZkniSHUT6Cb7L06Gg.png" width="60%" />

Usage:

```toml
[navigation]
mode = "CollapsedTab"
```

### NativeTab

The <span class="keyword">NativeTab</span> is Rio terminal default navigation mode for MacOs.

Note: NativeTab only works for MacOS.

<img alt="Demo NativeTab" src="/rio/assets/posts/0.0.17/demo-native-tabs.png" width="60%"/>

Usage:

```toml
[navigation]
mode = "NativeTab"
```

### BottomTab

Note: <span class="keyword">BottomTab</span> does not support click mode yet.

<img alt="Demo BottomTab" src="/rio/assets/features/demo-bottom-tab.png" width="58%"/>

Usage:

```toml
[colors]
tabs = "#000000"

[navigation]
mode = "BottomTab"
```

### TopTab

Note: <span class="keyword">TopTab</span> does not support click mode yet.

<img alt="Demo TopTab" src="/rio/assets/features/demo-top-tab.png" width="70%"/>

Usage:

```toml
[colors]
tabs = "#000000"

[navigation]
mode = "TopTab"
```

### Breadcrumb

Note: <span class="keyword">Breadcrumb</span> does not support click mode yet and is only available for MacOS, BSD and Linux.

<img alt="Demo Breadcrumb" src="/rio/assets/features/demo-breadcrumb.png" width="70%"/>

Usage:

```toml
[navigation]
mode = "Breadcrumb"
```

### Plain

Plain navigation mode will simply turn off any platform key binding, will not add any key binding (like creation of tabs, windows, panels and other platform key bindings).

This mode is perfect if you want set yourself how Rio key binding rules will work.

Usage:

```toml
[navigation]
mode = "Plain"
```

### Color automation for navigation

Rio allows to specify color overwrites for tabs based on program context.

The example below sets <span class="keyword">#FFFF00</span> as color background whenever <span class="keyword">nvim</span> is running.

<p>
<img alt="example navigation with color automation" src="/rio/assets/features/demo-colorized-navigation.png" width="48%"/>

<img alt="example navigation with color automation" src="/rio/assets/features/demo-colorized-navigation-2.png" width="48%"/>
</p>

The configuration would be like:

```toml
[navigation]
color-automation = [
  { program = "nvim", color = "#FFFF00" }
]
```
