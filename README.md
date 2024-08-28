# Open new window and send data from Vue (Vite)

1. Get reactive date with `v-model` on base window.
1. Create dom element (`id="result"`) with vue.
1. open new window with `window.open("./print_page.html", "newwindow")` .
1. From newly opened `print_page.html`, get vue-rendered data with `window.opener.document.querySelector("#result").innerHTML`.

---

Debug:

```
npm run dev
```


