<template>
    <div class="profile">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-lg-6">
                    <div class="media text-left">
                        <img src="../assets/ulhaq.png" class="mr-3 user-pic" alt="">
                        <div class="media-body">
                            <h5 class="mt-0">{{firstName}} {{lastName}}</h5>
                            <p>{{ket}}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
import "bootstrap/dist/css/bootstrap.css";
export default {
    name : "profile",
    data : function () {
        return{
            firstName : "Dhiya",
            lastName : "Ulhaq",
            ket : "Saya adalah seorang mahasiswa yang kuliah di universitas muslim indonesia, jurusan teknik informatika",
        }
    },
    components: {}
};
</script>

<style scoped>
    .user-pic {
        height: 80px;
        width: 80px;
        border-radius: 200%;
    }
</style>