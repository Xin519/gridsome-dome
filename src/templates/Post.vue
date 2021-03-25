<template>
  <Layout>

      <div class="journal" data-v-2a0eef53="">
			<div class="container " style="max-width:1200px">
				<div class="journal-header" data-v-2a0eef53="">
					<h1 class="journal-title" data-v-2a0eef53="">{{ $page.post.title }}</h1>
					<div class="journal-meta" data-v-2a0eef53="">
						<div class="journal-author" data-v-2a0eef53="">
							<span class="label" data-v-2a0eef53="">Author</span>
							<span class="author-name" >{{ $page.post.author }}</span>
						</div>
						<div class="journal-date" data-v-2a0eef53="">
							<span class="label" data-v-2a0eef53="">Date</span>
							<div data-v-2a0eef53="">{{ $page.post.date }}</div>
						</div>
						<!-- <div class="journal-time" data-v-2a0eef53="">
							<span class="label" data-v-2a0eef53="">Time</span>
							<span>1 min read 7. June 2019</span>
						</div> -->
					</div>
				</div>
				<div class="journal-content" data-v-2a0eef53="" style="margin-top:30px" v-html="mdToHtml($page.post.content)">
					
				</div>
			</div>
		</div>

  </Layout>
</template>

<page-query>
	query($id: ID){
		post: strapiPost(id: $id){
			title
			author
			content
			date
			
		}
	}
</page-query>

<script>
import MarkdownIt from 'markdown-it'
const md = new MarkdownIt()

export default {
    name:'post',
	methods:{
		mdToHtml(html){
			
			return html

		}
	}
}
</script>

<style>

</style>
