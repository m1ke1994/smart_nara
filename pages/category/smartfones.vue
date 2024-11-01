

<template>
    <div class="w-full m-10">
        <h1 class="text-3xl p-4 text-center">Ремонт смартфонов</h1>
        <hr>
        <div class="flex justify-center gap-4 flex-wrap py-4">
            <div class="items-center ">
                <select class=" py-2 px-3 border rounded-md outline-none bg-white">
                    <option class="sm:text-xs" value="">Выбирете из списка</option>
                    <option class="sm:text-xs" value="Samsung">Samsung</option>
                    <option class="sm:text-xs" value="Iphone">Iphone</option>
                    <option class="sm:text-xs" value="Xiaomi">Xiaomi</option>
                    <option class="sm:text-xs" value="Honor">Honor</option>
                    <option class="sm:text-xs" value="Tecno">Tecno</option>
                    <option class="sm:text-xs" value="Huawei">Huawei</option>
                    <option class="sm:text-xs" value="Realme">Realme</option>
                </select>
            </div>
            <div class="relative">
                <img class="absolute left-5 top-3 " src="/search.svg" alt="search">
                <input class="w-full border rounded-md py-2 pl-10 pr-4 outline-none focus:border-gray-400 pl-12  bg-white" type="text"
                    placeholder="Введите модель ...">
            </div>
            <div><button
                    class="bg-lime-600 border px-8 py-2 rounded-md hover:bg-lime-700 transition text-white">Найти</button>
            </div>
        </div>
        

    </div>

</template>