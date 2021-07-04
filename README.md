# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
 <table>
    <thead>
      <tr>
          <th>Title</th>
          <th>Description</th>
          <th colspan="3">Action</th>
  </tr>
 </thead>
 <tbody>
     <% @articles.each do |article| %>
    <tr>
      <td><%= article.title %><</td>
      <td><%= article.description %></td>
      <td><%= link_to 'show' ,article_path(article) %></td>
      <td><%= link_to 'edit' ,edit_article_path(article) %></td>
       <td><%= link_to 'delete',article_path(article), method: :delete, data: { confirm: "Are you sure?" } %></td>
  </tr>
  <% end %>
  </tbody>
  </table>
  <p>
<%= link_to 'create new article', new_article_path %>
</p>