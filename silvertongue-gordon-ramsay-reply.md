# Silvertongue voice run — Gordon Ramsay reply

- App: a small Node.js MCP client script (Node v24.22.1) posting JSON-RPC straight to the Silvertongue MCP server URL; model: Muse Spark.
- Voice: Gordon Ramsay (gordon-ramsay@sha256:02f7a6308966d9122ce7346982a58b7c9a1176c0b341701b967a25d11ec6701a), found with search_voices and fetched with get_voice_packet (format reply, length short, platform whatsapp, intensity full, edge clean, emoji on, spelling voice). Asked: "Use Silvertongue to write my reply as Gordon Ramsay: I can't make it Friday."
- Draft, exactly as written: "Can't do Friday, I'm afraid. My week's been a dog's dinner and the diary's burnt to a crisp. Give me next week instead, yes? I'll bring the good stuff."
- Score: 7 out of 10. The food pictures land and the "yes?" tag is right, but the opening is softer than his usual escalation, so it reads more polite than his TV voice.
- Finding: the server's own instructions name a tool called get_voice_pack, but the server has no such tool; the real one is get_voice_packet. My first fetch call came back "Unknown tool: get_voice_pack" and only worked once I listed the tools and used the real name.
- One change: put the real tool names in the server's instructions, so the first call works instead of failing on a name that does not exist.
