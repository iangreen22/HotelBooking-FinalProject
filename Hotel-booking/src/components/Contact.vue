<script>

</script>

<template>

    <section class="body-font relative my-10">

        <div class="container mx-auto px-5 py-24">

            <div class="mb-12 flex w-full flex-col text-center">
                <h1 class="mb-4 text-3xl sm:text-3xl text-black font-bold">Contact Us</h1>
                <p class="mx-auto text-base leading-relaxed lg:w-2/3">Feel free to reach out to us! Whether you have a
                    question,
                    feedback, we'd love to hear from you.
                </p>
            </div>

            <div class="mx-auto md:w-2/3 lg:w-1/2">
                <div class="-m-2 flex flex-wrap">

                    <!-- form -->
                    <div class="w-1/2 p-2">
                        <div class="relative">
                            <input type="text" id="name" name="name"
                                class="peer w-full rounded border border-gray-700 bg-black bg-opacity-40 py-1 px-3 text-base leading-8 text-gray-100 placeholder-transparent outline-none transition-colors duration-200 ease-in-out focus:border-indigo-500 focus:bg-gray-900 focus:ring-2 focus:ring-indigo-900"
                                placeholder="Name" />
                            <label for="name"
                                class="absolute left-3 -top-6 bg-transparent text-sm leading-7 text-indigo-500 transition-all peer-placeholder-shown:left-3 peer-placeholder-shown:top-2 peer-placeholder-shown:bg-gray-900 peer-placeholder-shown:text-base peer-placeholder-shown:text-gray-500 peer-focus:left-3 peer-focus:-top-6 peer-focus:text-sm peer-focus:text-indigo-500 px-2 rounded-md">Name</label>
                        </div>
                    </div>
                    <div class="w-1/2 p-2">
                        <div class="relative">
                            <input type="email" id="email" name="email"
                                class="peer w-full rounded border border-gray-700 bg-black bg-opacity-40 py-1 px-3 text-base leading-8 text-gray-100 placeholder-transparent outline-none transition-colors duration-200 ease-in-out focus:border-indigo-500 focus:bg-gray-900 focus:ring-2 focus:ring-indigo-900"
                                placeholder="Email" />
                            <label for="email"
                                class="absolute left-3 -top-6 bg-transparent text-sm leading-7 text-indigo-500 transition-all peer-placeholder-shown:left-3 peer-placeholder-shown:top-2 peer-placeholder-shown:bg-gray-900 peer-placeholder-shown:text-base peer-placeholder-shown:text-gray-500 peer-focus:left-3 peer-focus:-top-6 peer-focus:text-sm peer-focus:text-indigo-500 px-2 rounded-md">Email</label>
                        </div>
                    </div>
                    <div class="mt-4 w-full p-2">
                        <div class="relative">
                            <textarea id="message" name="message"
                                class="peer h-32 w-full resize-none rounded border border-gray-700 bg-black bg-opacity-40 py-1 px-3 text-base leading-6 text-gray-100 placeholder-transparent outline-none transition-colors duration-200 ease-in-out focus:border-indigo-500 focus:bg-gray-900 focus:ring-2 focus:ring-indigo-900"
                                placeholder="Message"></textarea>
                            <label for="message"
                                class="absolute left-3 -top-6 bg-transparent text-sm leading-7 text-indigo-500 transition-all peer-placeholder-shown:left-3 peer-placeholder-shown:top-2 peer-placeholder-shown:bg-gray-900 peer-placeholder-shown:text-base peer-placeholder-shown:text-gray-500 peer-focus:left-3 peer-focus:-top-6 peer-focus:text-sm peer-focus:text-indigo-500 px-2 rounded-md">Message</label>
                        </div>
                    </div>
                    <div class="w-full p-2">
                        <button
                            class="mx-auto flex rounded border-0 bg-black py-2 px-8 text-lg text-white hover:bg-gray-900 cursor-pointer focus:outline-none">Send</button>
                    </div>

                </div>
            </div>

        </div>

    </section>
</template>