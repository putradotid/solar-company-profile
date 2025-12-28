<template>
  <section class="max-w-4xl mx-auto px-6 py-24">
    <h1 class="text-4xl font-bold mb-6">Kontak Kami</h1>

    <form class="space-y-4 max-w-xl">
      <input
        type="text"
        placeholder="Nama"
        class="w-full border p-3 rounded"
      />
      <input
        type="email"
        placeholder="Email"
        class="w-full border p-3 rounded"
      />
      <textarea
        placeholder="Pesan"
        rows="4"
        class="w-full border p-3 rounded"
      ></textarea>

      <button
        type="submit"
        class="bg-black text-white px-6 py-3 rounded"
      >
        Kirim Pesan
      </button>
    </form>
  </section>
</template>
