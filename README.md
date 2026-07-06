# hadiamal1011.github.io
"use client";

import { useState } from "react";

export default function Home() {
  const [page, setPage] = useState(1);

  return (
    <main className="min-h-screen bg-pink-100 flex items-center justify-center p-6">
      <div className="bg-white rounded-3xl shadow-2xl p-8 w-full max-w-md text-center">

        {page === 1 && (
          <>
            <h1 className="text-4xl font-bold text-pink-600">
              Хадишка 💕
            </h1>

            <p className="mt-5 text-xl">
              Ты пойдёшь со мной на свидание?
            </p>

            <button
              onClick={() => setPage(2)}
              className="mt-8 w-full bg-pink-500 text-white rounded-xl p-4 text-xl"
            >
              Да 💖
            </button>
          </>
        )}

        {page === 2 && (
          <>
            <h1 className="text-3xl font-bold">
              Что будем кушать? 🍕
            </h1>

            <div className="grid grid-cols-2 gap-4 mt-6">

              <button
                onClick={() => setPage(3)}
                className="bg-pink-200 p-5 rounded-xl"
              >
                🍣 Суши
              </button>

              <button
                onClick={() => setPage(3)}
                className="bg-pink-200 p-5 rounded-xl"
              >
                🍕 Пицца
              </button>

              <button
                onClick={() => setPage(3)}
                className="bg-pink-200 p-5 rounded-xl"
              >
                🍔 Бургер
              </button>

              <button
                onClick={() => setPage(3)}
                className="bg-pink-200 p-5 rounded-xl"
              >
                🍰 Десерт
              </button>

            </div>
          </>
        )}

        {page === 3 && (
          <>
            <h1 className="text-3xl font-bold">
              Как поедем? 🚶
            </h1>

            <button
              onClick={() =>
                alert("❌ Нельзя. Нажми «Пойдём пешком за ручку» 🥹")
              }
              className="w-full mt-6 bg-white border rounded-xl p-4"
            >
              🚕 Закажешь Комфорт+
            </button>

            <button
              onClick={() =>
                alert("❌ Нет-нет 😼 Выбирай последний вариант")
              }
              className="w-full mt-4 bg-white border rounded-xl p-4"
            >
              🚗 Заберёшь меня сам
            </button>

            <button
              onClick={() => setPage(4)}
              className="w-full mt-4 bg-pink-500 text-white rounded-xl p-4"
            >
              💕 Пойдём пешком за ручку
            </button>
          </>
        )}

        {page === 4 && (
          <>
            <h1 className="text-4xl text-pink-600 font-bold">
              ❤️ Спасибо, Хадишка!
            </h1>

            <p className="mt-6 text-xl">
              Теперь официально идём на свидание 🌹
            </p>
          </>
        )}

      </div>
    </main>
  );
}

