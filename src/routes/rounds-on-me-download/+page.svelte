<script>
	const filePath = '/Windows1.4.zip';
</script>

<main class="pt-16">
    <div class="flex justify-center items-center min-h-screen">
        <div class="container mx-auto p-10">
            <h1 class="text-white text-5xl tracking-small text-center mb-4" id="recent-projects">
                <span
                    class="bg-gradient-to-br from-blue-500 to-cyan-300 bg-clip-text text-transparent box-decoration-clone"
                    >Rounds On Me</span
                >
            </h1>
            <!-- Moved the download button inside the container and directly below the text -->
            <div class="text-center">
                <a href={filePath} download="Windows1.4.zip" class="btn bg-gradient-to-br variant-gradient-secondary-tertiary p-7">
                    Download Game!
                </a>
            </div>
        </div>
    </div>
</main>
