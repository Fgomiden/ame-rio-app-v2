<template>
  <div class="flex items-top justify-center bg-white sm:items-center sm:pt-0">
    <div class="w-full">
      <div class="mt-8 overflow-hidden">
        <h2
          class="
            text-center text-3xl
            leading-8
            font-extrabold
            tracking-tight
            text-gray-900
          "
        >
          Fale Conosco
        </h2>
        <!-- md:grid-cols-2 -->
        <div class="grid grid-cols-1">
          <div class="p-6 mr-2 bg-gray-100 dark:bg-gray-800 sm:rounded-lg">
            <!-- <div
              class="
                flex
                justify-center
                items-center
                mt-8
                text-gray-600
                dark:text-gray-400
              "
            >
              <svg
                fill="none"
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="1.5"
                viewBox="0 0 24 24"
                class="w-8 h-8 text-gray-500"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="1.5"
                  d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"
                />
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="1.5"
                  d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"
                />
              </svg>
              <div class="ml-4 text-md tracking-wide font-semibold">
                Avenida Presidente Vargas, 446, Sala 605<br />Centro, Rio de
                Janeiro/RJ. CEP: 20071-000
              </div>
            </div> -->

            <div
              class="
                flex
                justify-center
                items-center
                mt-2
                text-gray-600
                dark:text-gray-400
              "
            >
              <svg
                fill="none"
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="1.5"
                viewBox="0 0 24 24"
                class="w-8 h-8 text-gray-500"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="1.5"
                  d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                />
              </svg>
              <div class="ml-4 text-md tracking-wide font-semibold">
                amecgs@gmail.com
              </div>
            </div>
          </div>

          <!-- <form class="p-6 flex flex-col justify-center">
            <div class="flex flex-col">
              <label for="name" class="hidden">Nome</label>
              <input
                type="name"
                name="name"
                id="name"
                placeholder="Nome"
                class="
                  w-100
                  mt-2
                  py-3
                  px-3
                  rounded-lg
                  bg-white
                  dark:bg-gray-800
                  border border-gray-400
                  dark:border-gray-700
                  text-gray-800
                  font-semibold
                  focus:border-indigo-500 focus:outline-none
                "
              />
            </div>

            <div class="flex flex-col mt-2">
              <label for="email" class="hidden">Email</label>
              <input
                type="email"
                name="email"
                id="email"
                placeholder="Email"
                class="
                  w-100
                  mt-2
                  py-3
                  px-3
                  rounded-lg
                  bg-white
                  dark:bg-gray-800
                  border border-gray-400
                  dark:border-gray-700
                  text-gray-800
                  font-semibold
                  focus:border-indigo-500 focus:outline-none
                "
              />
            </div>

            <div class="flex flex-col mt-2">
              <label for="tel" class="hidden">Assunto</label>
              <input
                type="tel"
                name="tel"
                id="tel"
                placeholder="Assunto"
                class="
                  w-100
                  mt-2
                  py-3
                  px-3
                  rounded-lg
                  bg-white
                  dark:bg-gray-800
                  border border-gray-400
                  dark:border-gray-700
                  text-gray-800
                  font-semibold
                  focus:border-indigo-500 focus:outline-none
                "
              />
            </div>

            <div class="flex flex-col mt-2">
              <textarea
                class="
                  appearance-none
                  block
                  w-full
                  py-3
                  px-4
                  leading-tight
                  text-gray-700
                  bg-gray-200
                  focus:bg-white
                  border border-gray-200
                  focus:border-gray-500
                  rounded
                  focus:outline-none
                "
                type="password"
                placeholder="Mensagem"
                rows="5"
                style="height: 146px"
              ></textarea>
            </div>

            <button
              type="submit"
              class="
                md:w-32
                bg-indigo-600
                hover:bg-blue-dark
                text-white
                font-bold
                py-3
                px-6
                rounded-lg
                mt-3
                hover:bg-indigo-500
                transition
                ease-in-out
                duration-300
              "
            >
              Submit
            </button>
          </form> -->
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'ContactForm',
}
</script>