## 💻 DevProfileCard.tsx

```tsx
import React from 'react';

type Dev = { name: string; skills: string[] };

const DevProfileCard = () => {
  const developer: Dev = {
    name: "João Pedro Machado",
    skills: [
      "Java & Spring Boot",
      "Node.js & Express",
      "React & JS/TS",
      "PostgreSQL & MySQL",
      "Bash & PowerShell"
    ],
  };

  return (
    <div className="relative rounded-lg bg-slate-900 p-4 text-white font-mono">
      <div className="flex items-center space-x-2 pb-2">
        <span className="h-3 w-3 rounded-full bg-red-500/20" />
        <span className="h-3 w-3 rounded-full bg-yellow-500/20" />
        <span className="h-3 w-3 rounded-full bg-green-500/20" />
        <span className="ml-2 text-xs text-slate-500">DevProfile.tsx</span>
      </div>

      <p className="text-xs text-violet-400">
        <span className="text-slate-500">Name:</span> <span className="text-blue-400">{developer.name}</span>
      </p>

      <p className="mt-2 text-xs text-violet-400">
        <span className="text-slate-500">Skills:</span>
        <ul className="list-disc list-inside mt-1 text-blue-400 space-y-0.5">
          {developer.skills.map((skill, index) => (
            <li key={index}>{skill}</li>
          ))}
        </ul>
      </p>
    </div>
  );
};

export default DevProfileCard;
