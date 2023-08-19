# JS-ModalProject
<p align="center">
  <img src="https://github.com/damlahub/JS-ModalProject/blob/main/ss.gif" alt="Sublime's custom image"/>
</p>

```ruby
let container = document.querySelector(".container");

function Show() {
    let div = document.createElement("div");
    div.classList.add("panel");
    div.onclick = ClosePanel;
    div.innerHTML = `
        <div class="message">
                <h1>Hi!</h1>
            </div>
    `;
    container.appendChild(div);
}
function ClosePanel(e) {
    let clickClass = e.target.classList;
    if (clickClass.contains("panel")) {
        e.target.style.animation = "close-fade 1s ease forwards";
        e.target.addEventListener("animationend", function () {
            e.target.remove();
        });
    }
}
```
