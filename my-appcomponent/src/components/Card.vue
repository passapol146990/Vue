<template>
  <div class="card">
    <img src="https://media.istockphoto.com/vectors/user-avatar-profile-icon-black-vector-illustration-vector-id1209654046?k=20&m=1209654046&s=612x612&w=0&h=Atw7VdjWG8KgyST8AXXJdmBkzn0lvgqyWod9vTb2XoE="/>
    <slot name="card-header"></slot>
    <slot name="card-body"></slot>
    <slot name="card-footer"></slot>
  </div>
</template>

<script>
export default {
  name: "CardVue",
};
</script>

<style>
.card {
  margin: 1rem 0;
  font-size: 1.25rem;
  font-weight: bold;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.3);
  padding: 0.5rem;
  color: #1f1f1f;
  border-radius: 25px;
  text-align: center;
}
img{
    widows: 100px;
    height: 100px;
}
</style>