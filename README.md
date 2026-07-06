# hadiamal1011.github.io
hadishka-ai/
├── app/
│   ├── page.tsx
│   ├── layout.tsx
│   └── api/chat/route.ts
├── components/
│   ├── Hero.tsx
│   ├── Food.tsx
│   ├── Transport.tsx
│   └── Final.tsx
├── public/
├── styles/
├── package.json
├── tailwind.config.ts
├── next.config.ts
└── .env.local
{
  "name": "hadishka-ai",
  "private": true,
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start"
  },
  "dependencies": {
    "next": "15",
    "react": "^19",
    "react-dom": "^19",
    "openai": "^5",
    "framer-motion": "^12",
    "tailwindcss": "^4"
  }
}
import OpenAI from "openai";

const openai = new OpenAI({
  apiKey: process.env.OPENAI_API_KEY,
});

export async function POST(req: Request) {
  const { message } = await req.json();

  const res = await openai.responses.create({
    model: "gpt-5",
    input: message,
  });

  return Response.json({ reply: res.output_text });
}
OPENAI_API_KEY