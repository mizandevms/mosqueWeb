<template>
	<section class="space-y-6 pb-10">
		<!-- 	hero section -->
		<div class="relative">
			<figure class="relative">
				<img class="h-[25rem] w-full object-cover" src="/images/Group 1.svg" alt="Background Image" />
			</figure>
			<marquee class="absolute bottom-2 z-10 space-x-4 py-2 bg-slate-500 bg-opacity-30 text-gray-50 font-semibold">
				<span>ফজর: ওয়াক্ত শুরু ৪:২৪ মিনিট, ওয়াক্ত শেষ ৫:৩৯ মিনিট। </span>
				<span> জোহর: ওয়াক্ত শুরু ১২:০২ মিনিট, ওয়াক্ত শেষ ৪:১১ মিনিট। </span>
				<span> আসর: ওয়াক্ত শুরু ৪:২৬ মিনিট, ওয়াক্ত শেষ ৬:১৫ মিনিট। </span>
				<span> মাগরিব: ওয়াক্ত শুরু ৬:২০ মিনিট, ওয়াক্ত শেষ ৬:৪০ মিনিট। </span>
				<span> ইশা: ওয়াক্ত শুরু ৭:৩৮ মিনিট, ওয়াক্ত শেষ ১১:৩০ মিনিট।</span>
			</marquee>
		</div>

		<!-- 3d Slider -->
		<div class="slider3d">
			<Slider :collections="mosques" />
		</div>

		<div class="container mx-auto">
			<div class="pb-4">
				<h2 class="text-3xl tracking-tight font-extrabold text-gray-900 sm:text-4xl">সাম্প্রতিক প্রকাশনা</h2>
				<p class="mt-3 text-lg text-gray-500 sm:mt-4">কোরআন নাজিলের মাস রমজান। রমজানে মহানবী (সা.) কোরআনচর্চায় অধিক মনোযোগী হতেন এবং নবীজি (সা.) ও জিবরাইল (আ.) পরস্পরকে কোরআন পাঠ করে শোনাতেন।.</p>
			</div>
			<div class="grid grid-cols-3 gap-x-4">
				<div class="flex flex-col rounded-lg shadow-lg overflow-hidden" v-for="blog in blogs" :key="blog">
					<div class="flex-shrink-0">
						<img class="h-48 w-full object-cover" :src="blog.imgUrl" alt="islamic book" />
					</div>
					<div class="flex-1 bg-white p-6 flex flex-col justify-between">
						<div class="flex-1">
							<p class="text-sm font-medium text-indigo-600">
								<a href="#" class="hover:underline"> Article </a>
							</p>
							<a href="#" class="block mt-2">
								<p class="text-xl font-semibold text-gray-900">{{ blog.title }}</p>
								<p class="mt-3 text-xs text-gray-500 text-justify">{{ blog.description }}.</p>
							</a>
						</div>
						<div class="mt-6 flex items-center">
							<div class="flex-shrink-0">
								<a href="#">
									<span class="sr-only">Brenna Goyette</span>
									<img class="h-10 w-10 rounded-full object-contain" src="https://images.unsplash.com/photo-1581294958576-36903fe82ed4?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8N3x8aW1hbXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60" alt="" />
								</a>
							</div>
							<div class="ml-3">
								<p class="text-sm font-medium text-gray-900">
									<a href="#" class="hover:underline"> {{ blog.author }} </a>
								</p>
								<div class="flex space-x-1 text-sm text-gray-500">
									<time datetime="2020-03-10"> Mar 10, 2020 </time>
									<span aria-hidden="true"> &middot; </span>
									<span> 4 min read </span>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>
<script>
import Slider from "../components/Slider3D.vue"

const mosques = [
	{
		imgUrl: "https://images.unsplash.com/flagged/photo-1558113118-e42e558b352a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NXx8bW9zcXVlc3xlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60",
	},
	{
		imgUrl: "https://images.unsplash.com/photo-1590092794015-bce5431c83f4?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8bW9zcXVlc3xlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60",
	},
	{
		imgUrl: "https://images.unsplash.com/photo-1511652019870-fbd8713560bf?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8OHx8bWFra2FoJTIwc2F1ZGklMjBhcmFiaWF8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60",
	},
	{
		imgUrl: "https://images.unsplash.com/photo-1604655983671-9d03650f604c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MzF8fG1ha2thaCUyMHNhdWRpJTIwYXJhYmlhfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
	},
]

const blogs = [
	{
		title: "কোরআন কেন শুনব, কিভাবে শুনব",
		description:
			"কোরআন নাজিলের মাস রমজান। রমজানে মহানবী (সা.) কোরআনচর্চায় অধিক মনোযোগী হতেন এবং নবীজি (সা.) ও জিবরাইল (আ.) পরস্পরকে কোরআন পাঠ করে শোনাতেন। আবদুল্লাহ ইবনে আব্বাস (রা.) বলেন, ‘রমজান মাসের প্রতি রাতে জিবরাইল (আ.) রাসুলুল্লাহ (সা.)-এর কাছে উপস্থিত হতেন এবং তাঁরা উভয়ই পবিত্র কোরআন তিলাওয়াত করে একে অপরকে শোনাতেন। ’ (বুখারি, হাদিস : ৬)এ জন্য আলেমরা রমজান মাসে কোরআন পাঠের ওপর যেমন তাগিদ দেন, তেমন তা শ্রবণ করাকেও গুরুত্বপূর্ণ মনে করেন।যারা সারা দিন তিলাওয়াতের সুযোগ পান না, তারা রমজানের রাতে তারাবিতে কোরআন তিলাওয়াত শুনতে পারেন।অন্যের তিলাওয়াত শুনতেন নবীজি (সা.) : আমর ইবনে মুররা (রা.) বলেন, নবী (সা.) আমাকে বললেন, আমার কাছে কোরআন পাঠ কোরো। আমি বললাম, আমি আপনার কাছে পাঠ করব? অথচ আপনার কাছেই তা অবতীর্ণ হয়েছে। তিনি বললেন, অন্যের মুখ থেকে শুনতে আমি পছন্দ করি। এরপর আমি তাঁর কাছে সুরা ‘নিসা’ পাঠ করলাম, যখন আমি ‘কাইফা ইজা জি’না মিন কুল্লি’ পর্যন্ত (৪১ নং আয়াত) পাঠ করলাম, তিনি বললেন—থামো, থামো। তখন তাঁর দুই চোখ থেকে টপ টপ করে অশ্রু ঝরছিল। (সহিহ বুখারি, হাদিস : ৪৫৮২)",
		author: "(সহিহ বুখারি, হাদিস : ৪৫৮২)",
		imgUrl: "https://images.unsplash.com/photo-1624862762003-8b04581301aa?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=942&q=80",
	},
	{
		title: "কোরআন কেন শুনব, কিভাবে শুনব",
		description:
			"কোরআন নাজিলের মাস রমজান। রমজানে মহানবী (সা.) কোরআনচর্চায় অধিক মনোযোগী হতেন এবং নবীজি (সা.) ও জিবরাইল (আ.) পরস্পরকে কোরআন পাঠ করে শোনাতেন। আবদুল্লাহ ইবনে আব্বাস (রা.) বলেন, ‘রমজান মাসের প্রতি রাতে জিবরাইল (আ.) রাসুলুল্লাহ (সা.)-এর কাছে উপস্থিত হতেন এবং তাঁরা উভয়ই পবিত্র কোরআন তিলাওয়াত করে একে অপরকে শোনাতেন। ’ (বুখারি, হাদিস : ৬)এ জন্য আলেমরা রমজান মাসে কোরআন পাঠের ওপর যেমন তাগিদ দেন, তেমন তা শ্রবণ করাকেও গুরুত্বপূর্ণ মনে করেন।যারা সারা দিন তিলাওয়াতের সুযোগ পান না, তারা রমজানের রাতে তারাবিতে কোরআন তিলাওয়াত শুনতে পারেন।অন্যের তিলাওয়াত শুনতেন নবীজি (সা.) : আমর ইবনে মুররা (রা.) বলেন, নবী (সা.) আমাকে বললেন, আমার কাছে কোরআন পাঠ কোরো। আমি বললাম, আমি আপনার কাছে পাঠ করব? অথচ আপনার কাছেই তা অবতীর্ণ হয়েছে। তিনি বললেন, অন্যের মুখ থেকে শুনতে আমি পছন্দ করি। এরপর আমি তাঁর কাছে সুরা ‘নিসা’ পাঠ করলাম, যখন আমি ‘কাইফা ইজা জি’না মিন কুল্লি’ পর্যন্ত (৪১ নং আয়াত) পাঠ করলাম, তিনি বললেন—থামো, থামো। তখন তাঁর দুই চোখ থেকে টপ টপ করে অশ্রু ঝরছিল। (সহিহ বুখারি, হাদিস : ৪৫৮২)",
		author: "(সহিহ বুখারি, হাদিস : ৪৫৮২)",
		imgUrl: "https://images.unsplash.com/photo-1551095581-a8e5b4b28558?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8N3x8aXNsYW1pYyUyMGJvb2tzfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
	},
	{
		title: "কোরআন কেন শুনব, কিভাবে শুনব",
		description:
			"কোরআন নাজিলের মাস রমজান। রমজানে মহানবী (সা.) কোরআনচর্চায় অধিক মনোযোগী হতেন এবং নবীজি (সা.) ও জিবরাইল (আ.) পরস্পরকে কোরআন পাঠ করে শোনাতেন। আবদুল্লাহ ইবনে আব্বাস (রা.) বলেন, ‘রমজান মাসের প্রতি রাতে জিবরাইল (আ.) রাসুলুল্লাহ (সা.)-এর কাছে উপস্থিত হতেন এবং তাঁরা উভয়ই পবিত্র কোরআন তিলাওয়াত করে একে অপরকে শোনাতেন। ’ (বুখারি, হাদিস : ৬)এ জন্য আলেমরা রমজান মাসে কোরআন পাঠের ওপর যেমন তাগিদ দেন, তেমন তা শ্রবণ করাকেও গুরুত্বপূর্ণ মনে করেন।যারা সারা দিন তিলাওয়াতের সুযোগ পান না, তারা রমজানের রাতে তারাবিতে কোরআন তিলাওয়াত শুনতে পারেন।অন্যের তিলাওয়াত শুনতেন নবীজি (সা.) : আমর ইবনে মুররা (রা.) বলেন, নবী (সা.) আমাকে বললেন, আমার কাছে কোরআন পাঠ কোরো। আমি বললাম, আমি আপনার কাছে পাঠ করব? অথচ আপনার কাছেই তা অবতীর্ণ হয়েছে। তিনি বললেন, অন্যের মুখ থেকে শুনতে আমি পছন্দ করি। এরপর আমি তাঁর কাছে সুরা ‘নিসা’ পাঠ করলাম, যখন আমি ‘কাইফা ইজা জি’না মিন কুল্লি’ পর্যন্ত (৪১ নং আয়াত) পাঠ করলাম, তিনি বললেন—থামো, থামো। তখন তাঁর দুই চোখ থেকে টপ টপ করে অশ্রু ঝরছিল। (সহিহ বুখারি, হাদিস : ৪৫৮২)",
		author: "(সহিহ বুখারি, হাদিস : ৪৫৮২)",
		imgUrl: "https://images.unsplash.com/photo-1626092811141-34babe0cb353?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTN8fGlzbGFtaWMlMjBib29rc3xlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60",
	},
]
export default {
	components: {
		Slider,
	},
	setup() {
		return {
			mosques,
			blogs,
		}
	},
}
</script>
<style scoped></style>
