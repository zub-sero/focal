Focal — Case Study
The problem
Getting useful feedback on a photograph is harder than it should be. Informal feedback tends to be encouraging but vague. Technical critique tends to be accurate but inaccessible. Neither tells you what to do differently next time.
Photography enthusiasts who want to improve deliberately face a specific problem: they are aware they can do better, but they cannot diagnose what to change, or why. And even when they get feedback on a single image, there is no way to know whether the issue is a one-off or a pattern in how they shoot.

What I built
Focal is an AI-powered photography critique tool that analyses images against core photography principles and tracks performance over time.
The tool does two things:
A single photo critique, where the user uploads an image, selects which principles they want assessed, and receives structured feedback: a short verdict followed by a principle-by-principle breakdown with specific improvement advice.
A skills profile, where the app remembers every critique a logged-in user has received, identifies recurring patterns across their photo history, and generates a coaching summary with a rating out of 10 per principle and a prioritised focus area.
Live at focalphoto.lovable.app

Who it is for
Photography enthusiasts who want to improve deliberately. Not beginners looking for encouragement, and not professionals who already know what they are doing. The target user is someone who shoots regularly, cares about getting better, and wants feedback that is specific enough to act on.

Key product decisions
Turning a snapshot tool into a coaching tool
The most important decision in this build was adding the skills profile. A single photo critique is a data point. An album of critiques tells a story about how someone shoots: what they consistently get right, where they repeatedly fall short, and what they should focus on next.
Without the skills profile, Focal answers a single question and stops. There is no reason to return, no accumulation of value over time, and no way for the user to know whether they are actually improving. The shift from single-session feedback to longitudinal coaching changed the entire value proposition.
Meeting users where they are
Early testing revealed a fundamental problem with AI photography feedback: it ignores context. A critique that tells a selfie photographer to move the camera back 30 centimetres is technically correct and completely useless.
The fix was a simple context selector added before the critique: was this a selfie, handheld by someone else, or shot on a tripod? That single input changes the nature of the feedback, keeping suggestions within what was actually possible when the photo was taken.
The principle selector
Rather than generating feedback across every photography principle by default, the tool lets users choose which principles they want assessed. This keeps feedback focused and respects the fact that different users care about different things. A street photographer and a portrait photographer are asking different questions of the same image.
What I cut
Multi-photo upload was scoped and cut. The value of batch upload is real but it adds interface complexity before the core single-photo flow has been validated. It is the first thing on the v2 list.
Video analysis was considered and rejected entirely. Video introduces different principles, different user needs, and a meaningfully different product. Adding it would have diluted the focus without serving the core user.

What I learned
The prompt is the product. The quality of the feedback depends almost entirely on the instructions given to the model. Small changes to how the prompt frames the task produce significantly different outputs. This is a product decision, not a technical one, and it deserves the same deliberate attention as any other feature.
Context changes everything. The selfie insight came from testing the product on a real photo and noticing that the feedback, while technically accurate, was not actually useful. The gap between correct and useful is where most AI product failures live.
Stateless tools have a ceiling. A tool that forgets everything the moment you close the tab can be useful but cannot be genuinely valuable over time. Adding authentication and a database backend was the decision that lifted this from a prototype into something with real product ambition.

What is next

Multi-photo upload for batch critique sessions
Usage history so users can review past critiques without regenerating them
Prompt versioning: treating the critique instructions as a versioned product artefact with a documented change history
A proper server-side API layer to remove the API key from the front end
