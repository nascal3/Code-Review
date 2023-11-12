### Code review
    <ul class="item-list"> 
        <% items.forEach((item) => { %>
            <li><%= item.name %></li>
        <% }); %>
    </ul>

- Using forEach for rendering is generally not advisable because `forEach` is designed for side effects.
-  It doesn't create a new array of elements, `forEach` mutates the existing array and doesn't return a new array.
-  Instead use `map`, it returns a new array of elements, each with a unique key. It is the easier to determine what has changed and update only the necessary parts of the DOM. 
-   `map` results in cleaner and more readable code and aligns with the principles that make React a powerful library for building user interfaces.

As shown in the code snippet below:

    <ul class="item-list"> 
        <% items.map((item, index) => { %>
            <li><%= item.name %></li>
        <% }); %>
    </ul>         
