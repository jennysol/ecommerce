<template>
	<v-app-bar
		absolute
		color="white"
		elevate-on-scroll
		scroll-target="#scrolling-techniques-7"
		class="mt-4"
	>
		<v-col cols="6">
			<h2 class="title mb-3">Hi, Dwight</h2>
			<v-row class="ml-0" data-app>
				<p class="subtitle">1725 Slough Avenue</p>
				<v-menu
					v-model="menu"
					:close-on-content-click="false"
					offset-y
				>
					<template v-slot:activator="{ on, attrs }">
						<v-btn
							v-bind="attrs"
							v-on="on"
							icon
							small
						>
							<v-icon class="mb-1" color="primary">mdi-chevron-down</v-icon>
						</v-btn>
					</template>

					<v-card elevation="0">
						<v-list elevation="0">
							<v-list-item>
								<v-list-item-avatar>
									<img
										src="https://gravatar.com/avatar/59d21f6eb25e2e74e513959c33003825?s=400&d=robohash&r=x"
										alt="Foto de perfil do usuário logado"
									>
								</v-list-item-avatar>

								<v-list-item-content>
									<v-list-item-title>Fracisco</v-list-item-title>
									<v-list-item-subtitle>francis2010@gmail.com</v-list-item-subtitle>
								</v-list-item-content>

								<v-list-item-action>
									<v-btn
										icon
										color="red"
										@click="menu = false"
									>
										<v-icon>mdi-close</v-icon>
									</v-btn>
								</v-list-item-action>
							</v-list-item>
						</v-list>
					</v-card>
				</v-menu>
			</v-row>
		</v-col>
		
		<v-spacer></v-spacer>

		<v-badge
			:content="messages"
			:value="messages"
			color="primary"
			overlap
		>
			<v-btn icon>
				<v-icon color="primary" large>mdi-cart-variant</v-icon>
			</v-btn>
		</v-badge>
		<v-icon class="ml-3" color="primary" large>mdi-emoticon-outline</v-icon>
	</v-app-bar>
</template>

<script>
export default {
  name: 'app-bar',
  data() {
		return {
			messages: 3,
      menu: false,
		}
  },
}
</script>
