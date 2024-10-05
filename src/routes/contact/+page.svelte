<script lang="ts">
    const contactLinks = [
      {
        name: "Facebook",
        imgSrc: "logo/facebook.png",
        url: "https://www.facebook.com/noeljohn.mateo/",
      },
      {
        name: "Instagram",
        imgSrc: "logo/instagram.png",
        url: "https://www.instagram.com/anuna.nol/",
      },
      {
        name: "GitHub",
        imgSrc: "logo/github.jpg",
        url: "https://github.com/NoLmuna",
      },
      {
        name: "Twitter",
        imgSrc: "logo/twitter.jpeg",
        url: "https://x.com/No_Lnga",
      },
    ];
  </script>
  
  <div class="w-full max-w-2xl grid md:grid-cols-1 gap-4 text-center">
    <h1 class="text-5xl mb-12">Contacts</h1>
    <p class="text-center mb-8">Feel free to contact me on my socials!</p>
    <div class="grid gap-8 grid-cols-2 md:grid-cols-4">
      {#each contactLinks as contact (contact.name)}
      <a href={contact.url} target="_blank" rel="noopener noreferrer" class="w-32 h-32 flex flex-col items-center">
        <img 
          src={contact.imgSrc} 
          alt={contact.name} 
          class="w-16 h-16 object-contain hover:scale-110 transition-transform duration-300"
        >
        <p class="mt-4 text-lg">{contact.name}</p>
      </a>
      {/each}
    </div>
  </div>