# bs3-upgrade

Bootstrap 3 upgrade library for spacings (margin, padding) and text aligment. For one element can use multiple classess.

---

# Margins and Paddings #

**Breakpoints**: 
- `xs`
- `sm`
- `md`
- `lg`

**Properties**:
- `m` - for classes that set margin <br>
- `p` - for classes that set padding

**Sides**:
- `t` - for classes that set margin-top or padding-top
- `b` - for classes that set margin-bottom or padding-bottom
- `l` - for classes that set margin-left or padding-left
- `r` - for classes that set margin-right or padding-right
- `x` - for classes that set both *-left and *-right
- `y` - for classes that set both *-top and *-bottom
- `leave blank` - for classes that set a margin or padding on all 4 sides of the element

	
**Sizes**: `0` - `100` with step `5`

#### Use: ####
Remember this pattern
```
col-{breakpoint}-{property}{side}-{size}
```

#### Examples: ####
- `col-xs-m-5` all 4 sides have margin 5px (works on `all` breakpoints)
- `col-lg-p-5` all 4 sides have padding 5px (works only on `lg` breakpoint)
- `col-md-mr-10` right side has margin 10px (works on `md` and `lg` breakpoints)
- `col-md-pr-10` right side has padding 10px (works on `md` and `lg` breakpoints)
- `col-lg-mx-15` right and left sides has margin 15px (for `lg` breakpoint)
- `col-lg-px-15` same as `col-lg-pr-15 col-lg-pl-15` - set right and left side padding 15px (for `lg` breakpoint)
- `col-lg-m-25` is same as `col-lg-mt-25 col-lg-mr-25 col-lg-mb-25 col-lg-ml-25`
- and so on ...

```html
...
<div class="row">
    <div class="col-lg-12 col-lg-m-25">
        now on breakpoint 'lg' all sides have margin 25px
    </div>
    <div class="col-lg-12 col-lg-mt-25 col-lg-mr-25 col-lg-mb-25 col-lg-ml-25">
        or like this
    </div>
</div>
...
```


---


# Text Aligment #

**Breakpoints**: 
- `xs`
- `sm`
- `md`
- `lg`

**Properties**: 
- `right`
- `left`
- `center`
- `justify`

#### Use: #### 
```
col-{breakpoint}-text-{property}
```

#### Example: ####
```
...
<div class="col-lg-12 col-xs-text-center">
    text centered on all breakpoints
</div>
...
```
```
...
<div class="col-lg-12 col-lg-text-center">
    text centered only on 'lg' breakpoint
</div>
...
```
```
...
<div class="col-lg-12 col-xs-text-center col-sm-text-left col-md-text-right col-lg-text-justify">
    each breakpoint have different text alignment
</div>
...
```