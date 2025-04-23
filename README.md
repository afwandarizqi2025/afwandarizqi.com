<button onclick="changeContent()">Ubah Konten</button>
<button onclick="toggleVisibility()">Tampilkan/Sembunyikan</button>
<button onclick="addAnimation()">Animasi Efek</button>

<div id="dynamicContent">Konten ini akan diubah secara dinamis.</div>

<form onsubmit="validateForm(event)">
    <label for="name">Nama:</label>
    <input type="text" id="name" name="name" required>
    <button type="submit">Kirim</button>
</form>

<script>
    function changeContent() {
        const content = document.getElementById('dynamicContent');
        content.innerHTML = 'Konten telah diperbarui!';
        content.classList.toggle('highlight');
    }

    function toggleVisibility() {
        const content = document.getElementById('dynamicContent');
        content.classList.toggle('hidden');
    }

    function addAnimation() {
        const content = document.getElementById('dynamicContent');
        content.classList.toggle('animate');
    }

    function validateForm(event) {
        event.preventDefault();
        const name = document.getElementById('name').value;
        if (name.trim() === '') {
            alert('Nama tidak boleh kosong!');
        } else {
            alert('Formulir berhasil dikirim!');
        }
    }
</script>
