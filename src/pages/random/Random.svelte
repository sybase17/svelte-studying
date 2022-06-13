<script>
    import { push } from 'svelte-spa-router';
    import Header from "../../components/Header.svelte";


    let members = [

    ];
    let inputName = "";
    let selectedMemberIndex = -1;
    let star = "";

    // メンバー追加ボタン
    function addMember() {
        if(inputName == "") {
            pass;
        }else{
            members = members.concat({name:inputName});
            inputName = "";
        }
    };

    // メンバー削除ボタン
    function deleteMember() {
        if(selectedMemberIndex >= 0){
            members.splice(selectedMemberIndex,1);
            members = members ;
            selectedMemberIndex = members.length -1;
        }
    }

    let  ismodal = true;

    // ルーレットボタン
    function myRandom() {
        let i = Math.floor( Math.random() * members.length);
        star = members[i].name;

        ismodal = !ismodal;
    }

    function close(){
		ismodal = !ismodal;
	}


    const onKeyPress = e => {
    if (e.charCode === 13) addMember();
  };

</script>

<Header/>
<main class="h-screen bg-yellow-50" >
    <div class="title">
        <h1 class="py-10 font-mono text-3xl shadow">My Svelte Random</h1>
    </div>

    <div class ="random-main  pt-10 pb-4">
        <select class=" shadow w-80" size=10  bind:value = {selectedMemberIndex}>
            {#each members as member , index}
                <option value={index}>{member.name}</option>
            {/each}
        </select>
    </div>

    <div class="tab">
		<button class="bg-green-600 py-2 px-4 text-white rounded shadow mt-4 " on:click={deleteMember}>削除</button>
		<input class="py-2 mx-4 shadow" type="text" placeholder="name" bind:value={inputName} on:keypress={onKeyPress} >
		<button class="bg-green-600 py-2 px-4 text-white rounded shadow mt-4"  on:click={addMember}>追加</button>
	</div>

    <div id ="mask" class:hidden={ismodal} class="fixed inset-0 bg-black z-10 bg-opacity-40" ></div>
	<section id="modal"  class="bg-white text-black w-96 px-10 py-5 rounded absolute top-64 right-0 left-52 mx-auto my-0 z-20 ease-in-out" class:hidden={ismodal} >
		<p>今日の司会者は{star}さんです</p>
		<button class="bg-gray-400 py-2 px-4 text-white rounded shadow mt-4" on:click={close}>閉じる</button>
	</section>


    <div class="mt-10">
		<button  on:click={myRandom} class="py-6 px-16 bg-green-600 text-white mt-10 rounded shadow text-2xl">ルーレットスタート!</button>
	</div>
</main>


<style>

    #modal.hidden {
		transform: translate(0 , -500px);
	}

</style>