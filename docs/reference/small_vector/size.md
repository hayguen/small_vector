---
title: size
parent: small_vector
---

# size

Retrieve the number of elements in the container.

{%- capture unified -%}
<span class="cpp20">constexpr</span>
size_type
size (void) const noexcept;
{%- endcapture -%}

{%- capture cpp20 -%}
constexpr
size_type
size (void) const noexcept;
{%- endcapture -%}

{%- capture cpp11 -%}
size_type
size (void) const noexcept;
{%- endcapture -%}

{% include prototype.html unified=unified cpp20=cpp20 cpp11=cpp11 %}

## Parameters

None.

## Return

The number of elements in the container.

## Complexity

𝓞(1).

## Exceptions

This function does not throw exceptions.

## Example

<div class="code-example" markdown="1">

{% capture ce-url %}
https://godbolt.org/#g:!((g:!((g:!((h:codeEditor,i:(filename:'1',fontScale:14,fontUsePx:'0',j:1,lang:c%2B%2B,selection:(endColumn:1,endLineNumber:1,positionColumn:1,positionLineNumber:1,selectionStartColumn:1,selectionStartLineNumber:1,startColumn:1,startLineNumber:1),source:'%23include+%3Chttps://raw.githubusercontent.com/gharveymn/small_vector/main/source/include/gch/small_vector.hpp%3E%0A%23include+%3Ciostream%3E%0A+%0Aint+%0Amain+(void)%0A%7B%0A++gch::small_vector%3Cint%3E+v%3B%0A++std::cout+%3C%3C+v.size+()+%3C%3C+std::endl%3B%0A%0A++v.push_back+(-1)%3B%0A++v.push_back+(-2)%3B%0A++v.push_back+(-3)%3B%0A++std::cout+%3C%3C+v.size+()+%3C%3C+std::endl%3B%0A%0A++v.clear+()%3B%0A++std::cout+%3C%3C+v.size+()+%3C%3C+std::endl%3B%0A%0A++return+0%3B%0A%7D%0A'),l:'5',n:'0',o:'C%2B%2B+source+%231',t:'0')),k:50,l:'4',m:100,n:'0',o:'',s:0,t:'0'),(g:!((g:!((h:compiler,i:(compiler:g112,filters:(b:'0',binary:'1',commentOnly:'0',demangle:'0',directives:'0',execute:'0',intel:'0',libraryCode:'0',trim:'1'),flagsViewOpen:'1',fontScale:14,fontUsePx:'0',j:1,lang:c%2B%2B,libs:!(),options:'',selection:(endColumn:1,endLineNumber:1,positionColumn:1,positionLineNumber:1,selectionStartColumn:1,selectionStartLineNumber:1,startColumn:1,startLineNumber:1),source:1,tree:'1'),l:'5',n:'0',o:'x86-64+gcc+11.2+(C%2B%2B,+Editor+%231,+Compiler+%231)',t:'0')),header:(),k:50,l:'4',m:50,n:'0',o:'',s:0,t:'0'),(g:!((h:output,i:(compiler:1,editor:1,fontScale:14,fontUsePx:'0',tree:'1',wrap:'1'),l:'5',n:'0',o:'Output+of+x86-64+gcc+11.2+(Compiler+%231)',t:'0')),header:(),l:'4',m:50,n:'0',o:'',s:0,t:'0')),k:50,l:'3',n:'0',o:'',t:'0')),l:'2',n:'0',o:'',t:'0')),version:4
{% endcapture %}

{% include compiler_explorer_link.html href=ce-url %}

<h3>Code</h3>

```c++
#include <gch/small_vector.hpp>
#include <iostream>
 
int 
main (void)
{
  gch::small_vector<int> v;
  std::cout << v.size () << std::endl;

  v.push_back (-1);
  v.push_back (-2);
  v.push_back (-3);
  std::cout << v.size () << std::endl;

  v.clear ();
  std::cout << v.size () << std::endl;

  return 0;
}
```

<h3>Output</h3>

```text
0
3
0
```

</div>

## See Also

- [gch::size()](non-member/size)
- [capacity()](capacity)