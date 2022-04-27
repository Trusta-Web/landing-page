<template>
  <body class="font-Lexend lg:ml-40 lg:mb-20 "  id="contact">
		<!-- Container -->
		<div class="container mt-10">
			<div class="flex justify-evenly px-6 my-12">
				<!-- Row -->
				<div class="w-full  lg:w-12/12 flex">
					<!-- Col -->
					<div
						class="lg:block lg:w-1/3 bg-cover rounded-l-lg"
						style="background-image: url('https://ik.imagekit.io/waknkqe0dx5v/Rocket_lqXwNYdbo.png?ik-sdk-version=javascript-1.4.3&updatedAt=1649337758747')"
					></div>
					<!-- Col -->
					<div class="w-full lg:w-7/12 bg-white p-5 rounded-lg lg:rounded-l-none">
						<form class="px-8 pt-6 pb-8 mb-4 bg-white rounded">
							<div class="mb-4">
								<h3 class="pt-4 text-2xl lg:text-4xl font-bold mb-2 lg:mb-5">Get in Touch !</h3>
								<label class="block mb-5 lg:mb-2 text-sm lg:text-md text-gray-500" >
									Accelerate your business now!
								</label>
								<input
									class="w-full px-3 py-2 mb-3 text-sm leading-tight text-gray-700 border rounded shadow appearance-none focus:outline-none focus:shadow-outline"
									id="email"
									type="email"
									placeholder="Email"
									v-model="email"
								/>
									<textarea v-model="message" placeholder="Message" class="w-full px-3 py-2 mb-3 text-sm leading-tight text-gray-700 border rounded shadow focus:outline-none focus:shadow-outline" rows="5"></textarea>
							</div>
							
							<div class="mb-6 ">
								<button
									class="w-3/7 px-4 py-2 font-bold text-white bg-blue-500 rounded-md hover:bg-blue-400 focus:outline-none focus:shadow-outline"
									type="button"
									@click="postEmail"
								>
									Send Message
								</button>
							</div>
						</form>
					</div>
				</div>
			</div>
		</div>
	</body>
</template>

<script>
import axios from 'axios'
import swal from 'sweetalert';
export default {
	data(){
		return{
			email: "",
			message: "",
			forEmail: "",
			forMessage: ""
		}
	},
	methods: {
		async postEmail(){
			if(this.message.length !== 0 && this.email.length !== 0){
				let result = await axios({
				method: 'POST',
				url: 'https://trusta-be.herokuapp.com/email',
				data: {
					message: this.message,
					email: this.email
				}
			})
				if(result){
					swal({icon:"success", text:"Thank you ! We'll reach out to you soon!"})
					this.forEmail = this.email
					this.forMessage = this.message
					this.message = ''
					this.email = ''
					let sendMail = await axios({
						method: "POST",
						url: "https://trusta-be.herokuapp.com/mail",
						data: {
							message: this.message,
							email: this.email
						}
					})
				}
			}else{
				swal("Email and Message cannot be empty!", {
					buttons: false,
					timer: 3000,
					});
			}
		}
	}
	
};
</script>

<style></style>
