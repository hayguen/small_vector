---
title: operator>
parent: Non-Member Functions
grand_parent: small_vector
---

# gch::operator> <span class="title-annotation">(deleted in C++20)</span>

Perform a lexicographical comparison of two containers to determine if the first
container is greater than the second.

{%- capture unified -%}
template <typename T, unsigned I, unsigned J, typename Allocator>
bool
operator> (const small_vector<T, I, Allocator>& lhs,
           const small_vector<T, J, Allocator>& rhs);
{%- endcapture -%}

{% include prototype.html unified=unified until=20 %}