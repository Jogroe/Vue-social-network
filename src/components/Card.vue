<template>
    <div id="card">
        <div id="card-info">
            <div id="card-info-user">
                <h3 id="h3-title">{{ data.pseudo }}</h3>
                <img id="user-image" src="../assets/images/user.png" />
            </div>
            <div id="card-info-date">
                <h4 id="h4-info">15/12/2022</h4>
            </div>
        </div>
        <div id="card-image">
            <img id="post-image" :src="data.urlImgArticle" />
        </div>
        <div id="card-description">
            <p id="description">{{ data.contenu }}</p>
        </div>
        <div id="card-counters">

        </div>
        <div id="card-comments">
            <div id="card-comments-title">
                <h3 id="h3-title">Commentaires : </h3>
            </div>
            <Comment v-for="comment in data.commentaires" :key="comment.id" :data="comment"></Comment>
            <div>
                <form id="form-comment">
                    <input id="form-comment-input" type="text" placeholder="Répondre" />
                    <input id="form-comment-submit" type="submit" />
                </form>
            </div>
        </div>
    </div>
</template>

<script setup>
    import Comment from './Comment.vue'

    const props = defineProps({
        data: Object
})
</script>

<style scoped>

#card {
    width: 100%;
    height: auto;
    border-radius: 10px;
    background-color: #15202B;
    border: 1px solid black;
    display: flex;
    flex-direction: column;
    margin-bottom: 15px;
}

#card-info {
    width: 100%;
    height: 80px;
    display: flex;
    flex-direction: row;
}

#card-info-user {
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
}

#h3-title {
    font-size: 30px;
    font-weight: 600;
    margin-left: 20px;
}

#h4-info {
    font-weight: 500;
    margin-right: 20px;
}

#user-image {
    width: 45px;
    height: 45px;
    margin-left: 10px;
}

#card-info-date {
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: row-reverse;
    align-items: center;
}

#card-image {
    width: 100%;
    height: 350px;
}

#post-image {
    width: 100%;
    height: 100%;
}

#card-description {
    width: 100%;
    height: auto;
}

#description {
    color: white;
    padding-left: 20px;
}

#card-counters {
    width: 100%;
    height: 50px;
    background-color: #15202B;
}

#card-comments {
    width: 100%;
    height: auto;
    display: flex;
    flex-direction: column;
}

#card-comments-title {
    width: 100%;
    height: 80px;
    display: flex;
    align-items: center;
    border-bottom: 1px solid black;
}

#form-comment-input {
    width: 97%;
    height: 35px;
    margin-bottom: 2px;
    border-radius: 5px;
    border: 1px solid grey;
    padding-left: 10px;
    font-size: 15px;
    font-weight: 600;
}

#form-comment-submit {
    width: 20%;
    height: 35px;
    border-radius: 5px;
    border: 1px solid black;
    font-size: 15px;
    font-weight: 600;
    background-color: rgb(29, 155, 240);
    color: white;
    cursor: pointer;
    margin-bottom: 20px;
}


</style>