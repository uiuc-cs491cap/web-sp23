+++
title = "Rotating Calipers"
author = ["Mattox Beckman"]
date = 2023-04-07
draft = false
+++

```c++ { linenos=true, linenostart=1 }
vector<point> p;

int n; // number of points

typedef pair<point,point> pp;

set<pp> antipodes;

int k=1;

while (dist(p[n],p[0],p[k+1]) > dist(p[n],p[1],p[k])
    ++k;

int i=1;
int j=k;

while (i <= k && j <= n) {
  antipodes.add(pp(p[i],p[k]));
  while (dist(p[i],p[i+1],p[j+1]) > dist(p[i],p[i+1],p[j]) && j<m) {
     antipodes.add(pp(p[i],p[j]));
     ++j;
  }
  ++i;
}
```
