<template>

<div>
  <div class="container">
    <div class="admin-posts">

      <h3>$ Categories </h3>

      <div class="add-category">
        <input type="text" placeholder="Category title">
        <a href="#" class="addCategory">+ create</a>
      </div>

      <CategoryTable/>

      <h3>$ Posts</h3>

      <div class="add-category">
        <input type="text" placeholder="Post title">
        <br>
        <input type="radio" id="male" name="gender" value="male">
        <label for="male">Scala</label>
        <input type="radio" id="female" name="gender" value="female">
        <label for="female">Javascript</label>
        <input type="radio" id="other" name="gender" value="other">
        <label for="other">Other</label>
        <div id="textBox" class="editable" contenteditable="true"></div>
        <label><input type="checkbox" name="switchMode" id="switchBox" onchange="setDocMode(this.checked);" />
          Display HTML </label>
        <span style="margin-left:32px">
                    <a href="#" class="addCategory" id="btnBlogTextArea">+ create draft</a>
                    <span style="color:white;padding:0 10px">/</span>
                    <a href="#" class="addCategory" id="btnBlogTextArea">+ publish</a>
                </span>
      </div>

      <table>
        <tr>
          <th><span class="table-title">Posts</span></th>
          <th><span class="table-title">Last Update</span></th>
          <th><span class="table-title">Actions</span></th>
          <th><span class="table-title">Status</span></th>
          <th><span class="table-title">Categories</span></th>
        </tr>
        <tr>
          <td><a class="title" href="#">Why should I learn Scala?</a></td>
          <td><span class="date">2021-03-23</span></td>
          <td> <a href="#" class="delete-btn">-d</a>|<a href="#" class="edit-btn">-e</a></td>
          <td><a class="title" href="#">Draft</a></td>
          <td><a class="title" href="#">Scala</a>, <a class="title" href="#">Javascript</a></td>
        </tr>
        <tr>
          <td><a class="title" href="#">Setting up Scala</a></td>
          <td><span class="date">2021-03-23</span></td>
          <td> <a href="#" class="delete-btn">-d</a>|<a href="#" class="edit-btn">-e</a></td>
          <td><a class="title" href="#">Draft</a></td>
          <td><a class="title" href="#">Javascript</a></td>
        </tr>
        <tr>
          <td><a class="title" href="#">Scala types</a></td>
          <td><span class="date">2021-03-23</span></td>
          <td> <a href="#" class="delete-btn">-d</a>|<a href="#" class="edit-btn">-e</a></td>
          <td><a class="title" href="#">Draft</a></td>
          <td><a class="title" href="#">Scala</a></td>
        </tr>
        <tr>
          <td><a class="title" href="#">Futures</a></td>
          <td><span class="date">2021-03-23</span></td>
          <td> <a href="#" class="delete-btn">-d</a>|<a href="#" class="edit-btn">-e</a></td>
          <td><a class="title" href="#">Published</a></td>
          <td><a class="title" href="#">Scala</a></td>
        </tr>
      </table>
    </div>
  </div>

</div>

</template>

<script>
import CategoryTable from "@/components/CategoryTable"

export default {
  name:"admin",
  components:{
    CategoryTable
  }
}

</script>

<style>
.admin-posts h3,
.admin-posts li {
  color: white;
  list-style: square;
  margin: 0;
  padding: 0;
}

.addCategory {
  color: greenyellow;
  cursor: pointer;
  font-size: 16px;
  text-decoration: none;
  transition: 0.3s;
}

.addCategory:hover {
  color: rgb(124, 124, 124);
}

.admin-posts small {
  font-weight: 200;
  font-size: 10px;
}

.admin-posts table {
  color: white
}

.admin-posts .date {
  color: white;
  font-size: 10px;
}

.admin-posts .title {
  color: yellow;
  font-size: 12px;
  font-weight: 500;
  text-decoration: none;
}

.admin-posts .table-title {
  color: gray;
  font-size: 12px;
  font-weight: 500;
  text-decoration: none;
}

.admin-posts table td {
  padding: 0 32px 0 0;
}

.admin-posts table {
  margin: 8px 0 32px 0;
}

.admin-posts .delete-btn {
  color: rgb(255, 138, 138);
  font-size: 12px;
  font-weight: 500;
  text-decoration: none;
  margin: 0 4px 0 0;
}

.admin-posts .edit-btn {
  color: rgb(255, 251, 31);
  font-size: 12px;
  font-weight: 500;
  text-decoration: none;
  margin: 0 0 0 4px;
}

.admin-posts .add-category {
  margin: 16px 0 32px 0;
}

.admin-posts textarea {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  height: 200px;
  width: 100%;
}

.admin-posts .editable {
  width: 100%;
  min-height: 80px;
  border: 1px solid #ccc;
  padding: 5px;
  background-color: white;
}

.admin-posts .html-content {
  color: white
}

label {
  color: white
}
</style>
