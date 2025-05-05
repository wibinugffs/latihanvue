    <script setup>
    import { ref, computed } from 'vue'

    // Menggunakan ref untuk menyimpan jumlah likes
    const likes = ref(0)

    // Membuat computed property untuk menampilkan "anjay" jika jumlah likes >= 10
    const jumlah = computed(() => {
        // Tampilkan "anjay" jika jumlah likes >= 10
        return likes.value >= 10 ? "anjay fastheng" : "likes 10x a"
    })

    // Fungsi untuk menambah likes
    const incrementLikes = () => {
    if (likes.value < 10) { // Jika likes < 10, increment likes
        likes.value++
    }
    }
    </script>

    <template>
    <div>
        <h2>{{ jumlah }}</h2> <!-- Menampilkan likes atau "anjay" di h2 -->
        <button @click="incrementLikes">Likes</button> <!-- Tombol untuk menambah likes -->
    </div>
    </template>
