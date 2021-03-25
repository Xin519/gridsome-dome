<template>
    <Layout>

        <div class="container" data-v-da896d1e="">
			<div class="journal-hero" data-v-da896d1e="">
				<h1 class="journal-header" data-v-da896d1e="">
					a wise person once said...
				</h1>
			</div>
		</div>

        <div>
            <template v-for="edge in $page.list.edges">
                <g-link data-v-da896d1e="" :to="'/post/' + edge.node.id" class="journal-post" v-if="edge.node.listDisplay" :key="edge.node.id">
                    <div data-v-da896d1e="" class="container journal">
                        <h2 data-v-da896d1e="" class="journal-title">
                            {{ edge.node.title }}
                        </h2>
                        <p data-v-da896d1e="" class="journal-excerpt">
                            Get up and running with Forestry CMS, a git-backed headless CMS with a slick editing interface.
                        </p>
                    </div>
                </g-link>
            </template>
            <!-- <a data-v-da896d1e="" href="./Details" class="journal-post">
                <div data-v-da896d1e="" class="container journal">
                    <h2 data-v-da896d1e="" class="journal-title">VueJS for your next project</h2>
                    <p data-v-da896d1e="" class="journal-excerpt">Vue (pronounced /vjuː/, like view) is a progressive framework for
                        building user interfaces.</p>
                </div>
            </a>
            <a data-v-da896d1e="" href="./Details" class="journal-post">
                <div data-v-da896d1e="" class="container journal">
                    <h2 data-v-da896d1e="" class="journal-title">macOS development environment</h2>
                    <p data-v-da896d1e="" class="journal-excerpt">Get up and running with a fresh macOS Catalina install</p>
                </div>
            </a>
            <a data-v-da896d1e="" href="./Details" class="journal-post">
                <div data-v-da896d1e="" class="container journal">
                    <h2 data-v-da896d1e="" class="journal-title">About Typography</h2>
                    <p data-v-da896d1e="" class="journal-excerpt">Font face, vertical rythm, readability, this long fake text should
                        flow.</p>
                </div>
            </a> -->
        </div>

    </Layout>
</template>

<page-query>
	query{
		list: allStrapiPost{
			edges{
				node{
					id
					title
					listDisplay
					author

				}
			}
		}
	}
</page-query>

<script>
export default {
    name:'journal'
}
</script>

<style>

</style>