<script lang="ts">
	let activeTab = $state('biography'); // Default olarak biyografi sekmesi açık

	// Biyografi verisi
	const biographyContent = $state({
		title: 'Prof. Dr. Fuat Sezgin (1924-2018)',
		highlights: [
			'İslam Bilim Tarihi Araştırmacısı',
			'Frankfurt Üniversitesi Arap-İslam Bilimleri Tarihi Enstitüsü Kurucusu',
			'İslam Bilim Tarihi Müzesi Kurucusu'
		],
		life: [
			{
				year: '1924',
				event: "Bitlis'te doğdu"
			},
			{
				year: '1943',
				event: "İstanbul Üniversitesi Şarkiyat Araştırmaları Enstitüsü'nde eğitime başladı"
			},
			{
				year: '1951',
				event: 'Doktorasını tamamladı'
			}
			// Daha fazla yaşam olayı eklenebilir
		],
		achievements: [
			'Geschichte des Arabischen Schrifttums (17 cilt)',
			'Science and Technology in Islam (5 cilt)',
			"İslam'da Bilim ve Teknik (5 cilt)"
		],
		gallery: [
			{
				id: 1,
				url: '/images/fuat-sezgin/calisma-masasi.jpg',
				caption: "Frankfurt Üniversitesi'ndeki çalışma masasında (1965)",
				category: 'academic'
			},
			{
				id: 2,
				url: '/images/fuat-sezgin/muzede.jpg',
				caption: "İslam Bilim Tarihi Müzesi'nde öğrencilerle (2010)",
				category: 'museum'
			},
			{
				id: 3,
				url: '/images/fuat-sezgin/kitaplar.jpg',
				caption: 'Geschichte des Arabischen Schrifttums eseri üzerinde çalışırken',
				category: 'research'
			},
			{
				id: 4,
				url: '/images/fuat-sezgin/konferans.jpg',
				caption: 'Bilim Tarihi Konferansında (1980)',
				category: 'academic'
			},
			{
				id: 5,
				url: '/images/fuat-sezgin/genclik.jpg',
				caption: 'İstanbul Üniversitesi yılları (1943)',
				category: 'youth'
			}
		]
	});

	// Tiyatro bölümü verisi
	const theaterContent = $state({
		title: "Fuat Sezgin'in Hayatını Anlatan Tiyatro Gösterisi",
		subtitle: 'Bilim Tarihine Adanmış Bir Ömür',
		acts: [
			{
				title: '1. Perde: Gençlik Yılları',
				description: "Bitlis'ten İstanbul'a uzanan yolculuk...",
				duration: '45 dakika',
				image: '/images/theater/act1.jpg',
				highlights: ['Çocukluk anıları', 'Eğitim hayatının başlangıcı', "İstanbul'a geliş"]
			},
			{
				title: '2. Perde: Akademik Hayat',
				description: 'Hellmut Ritter ile tanışma ve bilim tarihine adanmış bir ömür...',
				duration: '40 dakika',
				image: '/images/theater/act2.jpg',
				highlights: [
					'Hocası ile ilk karşılaşma',
					'Akademik çalışmaların başlangıcı',
					'Zorlu dönemler'
				]
			},
			{
				title: '3. Perde: Frankfurt Yılları',
				description: "Almanya'da geçen yıllar ve büyük başarılar...",
				duration: '35 dakika',
				image: '/images/theater/act3.jpg',
				highlights: ['Enstitünün kuruluşu', 'Büyük eserlerin yazımı', 'Dünya çapında tanınma']
			}
		],
		showDates: [
			{
				date: '15 Nisan 2024',
				time: '19:00',
				venue: 'Ana Salon',
				availability: 'Müsait'
			},
			{
				date: '16 Nisan 2024',
				time: '20:00',
				venue: 'Ana Salon',
				availability: 'Son Biletler'
			},
			{
				date: '17 Nisan 2024',
				time: '19:00',
				venue: 'Ana Salon',
				availability: 'Müsait'
			}
		],
		cast: [
			{
				name: 'Ahmet Yılmaz',
				role: 'Genç Fuat Sezgin',
				image: '/images/theater/cast1.jpg'
			},
			{
				name: 'Mehmet Demir',
				role: 'Olgun Fuat Sezgin',
				image: '/images/theater/cast2.jpg'
			},
			{
				name: 'Ayşe Kaya',
				role: 'Ursula Sezgin',
				image: '/images/theater/cast3.jpg'
			}
		],
		gallery: [
			{
				url: '/images/theater/rehearsal1.jpg',
				caption: 'Provalardan bir kare'
			},
			{
				url: '/images/theater/rehearsal2.jpg',
				caption: 'Kostüm provaları'
			},
			{
				url: '/images/theater/stage.jpg',
				caption: 'Sahne tasarımı'
			}
		]
	});

	// Okul çalışmaları verisi
	const schoolContent = $state({
		title: "Fuat Sezgin'i Anma ve Anlama Çalışmalarımız",
		description:
			"Okulumuzda yürütülen projeler ve etkinlikler ile Prof. Dr. Fuat Sezgin'in mirasını yaşatıyoruz.",
		stats: [
			{ label: 'Aktif Proje', value: '4' },
			{ label: 'Katılımcı Öğrenci', value: '150+' },
			{ label: 'Yıllık Etkinlik', value: '12' },
			{ label: 'Bilim Tarihi Eseri', value: '200+' }
		],
		projects: [
			{
				title: 'Bilim Tarihi Kulübü',
				description: "Öğrencilerimizin Fuat Sezgin'in eserlerini incelediği haftalık toplantılar",
				participants: 25,
				status: 'active',
				image: '/images/school/science-club.jpg',
				video: {
					url: 'https://www.youtube.com/embed/VIDEO_ID',
					title: 'Kulüp Tanıtım Videosu'
				},
				activities: ['Haftalık okuma grupları', 'Bilim tarihi sunumları', 'Müze ziyaretleri']
			},
			{
				title: 'Fuat Sezgin Köşesi',
				description: 'Okul kütüphanemizde oluşturulan özel bölüm',
				collection: '150+ kitap',
				status: 'completed',
				image: '/images/school/library-corner.jpg',
				video: {
					url: 'https://www.youtube.com/embed/VIDEO_ID',
					title: 'Kütüphane Tanıtımı'
				},
				activities: ['Dijital katalog sistemi', 'Öğrenci araştırma projeleri', 'Sergi alanı']
			},
			{
				title: 'Yıllık Anma Etkinlikleri',
				description: 'Her yıl düzenlenen konferans ve sergiler',
				lastEvent: '30 Haziran 2023',
				nextEvent: '30 Haziran 2024',
				image: '/images/school/annual-event.jpg',
				video: {
					url: 'https://www.youtube.com/embed/VIDEO_ID',
					title: 'Geçen Yılki Etkinlikten Kesitler'
				},
				activities: ['Konferanslar', 'Öğrenci sunumları', 'İnteraktif sergiler']
			}
		],
		upcomingEvents: [
			{
				title: 'Bilim Tarihi Semineri',
				date: '15 Nisan 2024',
				time: '14:00',
				location: 'Konferans Salonu',
				speaker: 'Prof. Dr. Ahmet Yılmaz'
			},
			{
				title: 'Öğrenci Projeleri Sergisi',
				date: '20 Nisan 2024',
				time: '10:00',
				location: 'Sergi Salonu',
				duration: '3 gün'
			}
		]
	});

	// Tab değiştirme fonksiyonu
	async function switchTab(tab: string) {
		activeTab = tab;
	}
</script>

<!-- Arka plan div'i -->
<div class="bg-image"></div>

<!-- Ana container'ı güncelliyoruz -->
<main class="relative min-h-screen px-4 py-8">
	<!-- Yarı saydam overlay -->
	<div class="fixed inset-0 z-0"></div>

	<!-- İçerik -->
	<div class="container relative z-10 mx-auto">
		<h1 class="mb-8 text-center text-5xl font-bold tracking-tight text-blue-800">
			Prof. Dr. Fuat Sezgin
		</h1>

		<!-- Navigation Tabs -->
		<div class="mb-8 flex flex-wrap justify-center gap-4">
			{#each ['biography', 'theater', 'school'] as tab}
				<button
					class="w-full rounded-lg px-4 py-3 font-medium transition-all duration-300 sm:w-auto sm:px-6
						   {activeTab === tab
						? 'scale-105 bg-blue-600 text-white shadow-lg'
						: 'bg-white text-gray-700 hover:bg-gray-100'}"
					onclick={() => switchTab(tab)}
				>
					{#if tab === 'biography'}
						Hayatı ve Çalışmaları
					{:else if tab === 'theater'}
						Tiyatro Bölümü
					{:else}
						Okul Çalışmaları
					{/if}
				</button>
			{/each}
		</div>

		<!-- Content Sections -->
		<div class="rounded-xl bg-white/80 p-8 shadow-lg transition-all duration-300">
			{#if activeTab === 'biography'}
				<div class="space-y-6">
					<h2 class="text-3xl font-bold text-gray-800">{biographyContent.title}</h2>

					<div class="my-4 flex flex-wrap gap-4">
						{#each biographyContent.highlights as highlight}
							<span class="rounded-full bg-blue-100 px-3 py-1 text-sm text-blue-800">
								{highlight}
							</span>
						{/each}
					</div>

					<div class="space-y-4">
						<h3 class="text-xl font-semibold text-gray-700">Yaşam Kronolojisi</h3>
						<div class="space-y-2">
							{#each biographyContent.life as { year, event }}
								<div class="flex items-center gap-4">
									<span class="font-bold text-blue-600">{year}</span>
									<span class="text-gray-700">{event}</span>
								</div>
							{/each}
						</div>
					</div>

					<div class="space-y-4">
						<h3 class="text-xl font-semibold text-gray-700">Önemli Eserleri</h3>
						<ul class="list-inside list-disc space-y-2">
							{#each biographyContent.achievements as achievement}
								<li class="text-gray-700">{achievement}</li>
							{/each}
						</ul>
					</div>

					<!-- Fotoğraf Galerisi -->
					<div class="mt-8">
						<h3 class="mb-6 text-xl font-semibold text-gray-700">Fotoğraf Galerisi</h3>
						<div class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3">
							{#each biographyContent.gallery as photo}
								<div class="group relative overflow-hidden rounded-xl">
									<img
										src={photo.url}
										alt={photo.caption}
										class="h-64 w-full object-cover transition-transform duration-300 group-hover:scale-105"
									/>
									<div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent">
										<p class="absolute bottom-4 left-4 right-4 text-sm text-white">
											{photo.caption}
										</p>
									</div>
									<div class="absolute right-2 top-2">
										<span
											class="rounded-full bg-white/80 px-3 py-1 text-xs font-medium text-gray-800"
										>
											{photo.category}
										</span>
									</div>
								</div>
							{/each}
						</div>
					</div>

					<!-- Hero Section - Üst kısma eklenebilir -->
					<div class="mb-8 grid gap-8 lg:grid-cols-2">
						<div class="relative h-96 overflow-hidden rounded-xl">
							<img
								src="/images/fuat-sezgin/hero.jpg"
								alt="Prof. Dr. Fuat Sezgin"
								class="h-full w-full object-cover"
							/>
						</div>
						<div class="flex flex-col justify-center space-y-4">
							<h2 class="text-3xl font-bold text-gray-800">{biographyContent.title}</h2>
							<div class="flex flex-wrap gap-4">
								{#each biographyContent.highlights as highlight}
									<span class="rounded-full bg-blue-100 px-3 py-1 text-sm text-blue-800">
										{highlight}
									</span>
								{/each}
							</div>
							<p class="text-gray-600">
								Prof. Dr. Fuat Sezgin, İslam bilim tarihine adanmış bir ömrün temsilcisidir. Bilim
								tarihine yaptığı katkılarla dünya çapında tanınan bir bilim insanı olmuştur.
							</p>
						</div>
					</div>
				</div>
			{:else if activeTab === 'theater'}
				<div class="space-y-12">
					<!-- Hero Section -->
					<div class="relative mb-12 h-96 overflow-hidden rounded-2xl">
						<img
							src="/images/theater/hero.jpg"
							alt="Tiyatro gösterisi"
							class="h-full w-full object-cover"
						/>
						<div class="absolute inset-0 bg-gradient-to-t from-black/80 to-transparent">
							<div class="absolute bottom-8 left-8 right-8">
								<h2 class="text-4xl font-bold text-white">{theaterContent.title}</h2>
								<p class="mt-2 text-xl text-gray-200">{theaterContent.subtitle}</p>
							</div>
						</div>
					</div>

					<!-- Perdeler -->
					<section class="space-y-8">
						<h3 class="text-2xl font-bold text-gray-800">Oyun Akışı</h3>
						<div class="grid gap-8 md:grid-cols-3">
							{#each theaterContent.acts as act}
								<div
									class="group overflow-hidden rounded-xl bg-white shadow-lg transition-all hover:shadow-xl"
								>
									<div class="relative h-48">
										<img
											src={act.image}
											alt={act.title}
											class="h-full w-full object-cover transition-transform duration-300 group-hover:scale-105"
										/>
										<div class="absolute bottom-0 w-full bg-gradient-to-t from-black/60 p-4">
											<p class="text-lg font-semibold text-white">{act.title}</p>
											<p class="text-sm text-gray-200">{act.duration}</p>
										</div>
									</div>
									<div class="p-4">
										<p class="text-gray-600">{act.description}</p>
										<ul class="mt-4 space-y-2">
											{#each act.highlights as highlight}
												<li class="flex items-center text-sm text-gray-600">
													<span class="mr-2 text-blue-500">•</span>
													{highlight}
												</li>
											{/each}
										</ul>
									</div>
								</div>
							{/each}
						</div>
					</section>

					<!-- Gösterim Tarihleri -->
					<section class="space-y-6">
						<h3 class="text-2xl font-bold text-gray-800">Gösterim Tarihleri</h3>
						<div class="grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
							{#each theaterContent.showDates as show}
								<div class="flex items-center justify-between rounded-lg bg-gray-50 p-4">
									<div>
										<p class="font-semibold text-gray-800">{show.date}</p>
										<p class="text-sm text-gray-600">{show.time} - {show.venue}</p>
									</div>
									<span class="rounded-full bg-blue-100 px-3 py-1 text-sm text-blue-800">
										{show.availability}
									</span>
								</div>
							{/each}
						</div>
					</section>

					<!-- Oyuncu Kadrosu -->
					<section class="space-y-6">
						<h3 class="text-2xl font-bold text-gray-800">Oyuncu Kadrosu</h3>
						<div class="grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
							{#each theaterContent.cast as actor}
								<div class="group relative overflow-hidden rounded-lg">
									<img
										src={actor.image}
										alt={actor.name}
										class="h-72 w-full object-cover transition-transform duration-300 group-hover:scale-105"
									/>
									<div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent">
										<div class="absolute bottom-4 left-4">
											<p class="text-lg font-semibold text-white">{actor.name}</p>
											<p class="text-sm text-gray-200">{actor.role}</p>
										</div>
									</div>
								</div>
							{/each}
						</div>
					</section>

					<!-- Galeri -->
					<section class="space-y-6">
						<h3 class="text-2xl font-bold text-gray-800">Provalardan Kareler</h3>
						<div class="grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
							{#each theaterContent.gallery as photo}
								<div class="group relative overflow-hidden rounded-lg">
									<img
										src={photo.url}
										alt={photo.caption}
										class="h-64 w-full object-cover transition-transform duration-300 group-hover:scale-105"
									/>
									<div
										class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent opacity-0 transition-opacity group-hover:opacity-100"
									>
										<p class="absolute bottom-4 left-4 right-4 text-sm text-white">
											{photo.caption}
										</p>
									</div>
								</div>
							{/each}
						</div>
					</section>
				</div>
			{:else if activeTab === 'school'}
				<div class="space-y-12">
					<!-- Hero Section -->
					<div
						class="relative rounded-2xl bg-gradient-to-r from-blue-600 to-blue-800 p-8 text-white"
					>
						<div class="grid gap-8 md:grid-cols-2">
							<div class="space-y-4">
								<h2 class="text-3xl font-bold">{schoolContent.title}</h2>
								<p class="text-lg text-blue-100">{schoolContent.description}</p>
							</div>
							<div class="grid grid-cols-2 gap-4">
								{#each schoolContent.stats as stat}
									<div class="rounded-lg bg-white/10 p-4 backdrop-blur">
										<div class="text-2xl font-bold">{stat.value}</div>
										<div class="text-sm text-blue-100">{stat.label}</div>
									</div>
								{/each}
							</div>
						</div>
					</div>

					<!-- Projeler -->
					<section class="space-y-8">
						<h3 class="text-2xl font-bold text-gray-800">Projelerimiz</h3>
						<div class="grid gap-8 lg:grid-cols-3">
							{#each schoolContent.projects as project}
								<div class="group rounded-xl bg-white p-6 shadow-lg transition-all hover:shadow-xl">
									<!-- Proje Görseli -->
									<div class="relative mb-4 aspect-video overflow-hidden rounded-lg">
										<img
											src={project.image}
											alt={project.title}
											class="h-full w-full object-cover transition-transform duration-300 group-hover:scale-105"
										/>
										{#if project.status === 'active'}
											<div class="absolute right-2 top-2">
												<span class="rounded-full bg-green-500 px-3 py-1 text-sm text-white">
													Aktif Proje
												</span>
											</div>
										{/if}
									</div>

									<!-- Proje Bilgileri -->
									<h4 class="mb-2 text-xl font-semibold text-gray-800">{project.title}</h4>
									<p class="mb-4 text-gray-600">{project.description}</p>

									<!-- Video -->
									{#if project.video}
										<div class="mb-4 aspect-video w-full">
											<iframe
												title={project.video.title}
												src={project.video.url}
												class="h-full w-full rounded-lg"
												allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
												allowfullscreen
											></iframe>
										</div>
									{/if}

									<!-- Aktiviteler -->
									<div class="space-y-2">
										<h5 class="font-semibold text-gray-700">Aktiviteler:</h5>
										<ul class="space-y-1">
											{#each project.activities as activity}
												<li class="flex items-center text-sm text-gray-600">
													<span class="mr-2 text-blue-500">•</span>
													{activity}
												</li>
											{/each}
										</ul>
									</div>

									<!-- Proje Detayları -->
									<div class="mt-4 flex flex-wrap gap-2">
										{#if project.participants}
											<span class="rounded bg-blue-100 px-2 py-1 text-sm text-blue-800">
												{project.participants} Katılımcı
											</span>
										{/if}
										{#if project.collection}
											<span class="rounded bg-purple-100 px-2 py-1 text-sm text-purple-800">
												{project.collection}
											</span>
										{/if}
									</div>
								</div>
							{/each}
						</div>
					</section>

					<!-- Yaklaşan Etkinlikler -->
					<section class="space-y-6">
						<h3 class="text-2xl font-bold text-gray-800">Yaklaşan Etkinlikler</h3>
						<div class="grid gap-4 sm:grid-cols-2">
							{#each schoolContent.upcomingEvents as event}
								<div class="rounded-lg border border-blue-100 bg-blue-50 p-4">
									<h4 class="text-lg font-semibold text-blue-800">{event.title}</h4>
									<div class="mt-2 space-y-1 text-sm text-gray-600">
										<p class="flex items-center">
											<span class="mr-2">📅</span>
											{event.date} - {event.time}
										</p>
										<p class="flex items-center">
											<span class="mr-2">📍</span>
											{event.location}
										</p>
										{#if event.speaker}
											<p class="flex items-center">
												<span class="mr-2">👤</span>
												{event.speaker}
											</p>
										{/if}
										{#if event.duration}
											<p class="flex items-center">
												<span class="mr-2">⏱️</span>
												{event.duration}
											</p>
										{/if}
									</div>
								</div>
							{/each}
						</div>
					</section>
				</div>
			{/if}
		</div>
	</div>
</main>

<style>
	.bg-image {
		background-image: url('/bg-photo.webp');
		background-size: cover;
		background-position: center;
		background-attachment: fixed;
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		z-index: -1;
	}
</style>
