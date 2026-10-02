```dataviewjs
const applyTheme = () => {
    const file = app.workspace.getActiveFile();
    if (!file) return;

    document.body.classList.remove("cp1", "cp2", "cp3", "cp4", "cp5", "nav");

    const path = file.path;

    if (path.startsWith("cp1 - Start/")) {
        document.body.classList.add("cp1");
    }
    else if (path.startsWith("cp2 - Feeling Purple/")) {
        document.body.classList.add("cp2");
    }
    else if (path.startsWith("cp3 - Scared of Red/")) {
        document.body.classList.add("cp3");
    }
    else if (path.startsWith("cp4 - Crimson Nightmares/")) {
        document.body.classList.add("cp4");
    }
    else if (path.startsWith("cp5 - Too Deep to Think/")) {
        document.body.classList.add("cp5");
    }
    else {
        document.body.classList.add("nav");
    }
};

applyTheme();

app.workspace.on("active-leaf-change", applyTheme);
```
(please dont mess with this file :D)