<template>
    <div class="container">
        <header>
            <div class="px-3 py-2 bg-dark text-white">
            <div class="container">
                <div class="d-flex flex-wrap align-items-center justify-content-center justify-content-lg-start">
                <router-link to="/" class="d-flex align-items-center my-2 my-lg-0 me-lg-auto text-white text-decoration-none">
                    Домой
                </router-link>
                <ul class="nav col-12 col-lg-auto my-2 justify-content-center my-md-0 text-small">
                    <li>
                        <router-link to="/login" class="nav-link text-white" style="text-decoration: none; color: white;">
                            Войти
                        </router-link>
                    </li>
                    <li>
                        <a @click.prevent="logout" class="nav-link text-white" href="#">Выйти</a>
                    </li>
                    <li>
                        <router-link to="/register" class="nav-link text-white" style="text-decoration: none; color: white;">
                            Регистрация
                        </router-link>
                    </li>
                </ul>
                </div>
            </div>
            </div>
        </header>
        
        <main class="py-5">
            <router-view></router-view>
        </main>
    </div>
</template>

<script>
    import axios from 'axios';
    export default {
        name: 'App',
        methods: {
            logout() {
                axios.post('/logout').then(res => {
                    localStorage.removeItem('token');
                    this.$router.push({name: 'login'});
                })
            }
            
        }
    }
</script>