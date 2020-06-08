<template>
   <div>
   		<g-link class="post-tags__link" v-for="tag in post.tags" :key="tag.id" :to="tag.path">
   			<v-chip><span>#</span> {{ tag.title }} </v-chip>
   		</g-link>
    </div>
</template>

<script>
export default {
  props: ['post']
}
</script>

<style lang="scss">
.post-tags {
  margin: 1em 0 0;

  &__link {
  	margin-right: .7em;
  	font-size: .8em;
  	color: currentColor;
  	text-decoration: none;
  	padding: .5em;
  	border-radius: var(--radius);
  }
}
</style>