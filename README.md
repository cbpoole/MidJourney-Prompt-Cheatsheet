# Basic Prompt Anatomy: 
---

`/imagine prompt:` `[PREFIX]` `[SCENE]` `[SUFFIX]` `--[Parameters]`  
  
  - `PREFIX`: defines image medium & style.
  - `SCENE`: defines content.
  - `SUFFIX`: modulates Prefix & Scene

> NOTE: *in actual practice these categories overlap*

```
Permutation Prompt Example:
/imagine prompt: cinematic shot of astronaut on {horse, turtle} --c {20,80}
...gets translated into four prompts:
->   cinematic shot of astronaut on a horse --c 20
     cinematic shot of astronaut on a turtle --c 20
     cinematic shot of astronaut on a horse --c 80
     cinematic shot of astronaut on a turtle --c 80  
Basic Parameters:
--ar [WIDTH:HEIGHT]   (=aspect ratio)
--c [0-100]           (=chaos, unusual results)
--q [.25|.5|1]        (=quality/time spent generating the image, 1=default)
--seed [0-4294967295] (=starting point for initial grid)
--stop [10-100]       (=stop at earlier percentage)
--s [0-1000]          (=stylize, artistic interpretation)
--tile                (=seamless patterns)
--iw [W]              (=sets image weight to W)
--no [X]              (=gives X a negative weight of -0.5)
--repeat [N]          (=repeat prompt N-times)
--video               (=create movie of image generation)
Version Parameters:
--v [1,2,3,4,5,5.1,5.2] (=model version)
--style raw             (artistic fine-tuning for V5.1 & V5.2)
--style [4a, 4b, 4c]    (artistic fine-tuning for V4)
--test, --testp, --creative (=test models, legacy)
Niji Parameters:
--niji / --niji 5     (anime trained model)
Niji Style Options:
--style cute
--style expressive
--style sceenic
--style original
Weights:
/imagine prompt:       hot dog
                       hot:: dog
                       hot::2 dog
Option Commands:
/prefer option set [NAME OF OPTION] [VALUE]
  ... e.g:
  ->     /prefer option set mycoolpreset dadaism --c 80
         ...now
         /imagine prompt: an astronaut, --mycoolpreset
         ...becomes
         /imagine prompt: an astronaut, dadaism --c 80
/prefer option set mycoolpreset
     ...deletes mycoolpreset!
/prefer option list
     ... shows presets
/prefer option remix
     ... toggles remix mode
/prefer suffix 
     ... suffix to add to the end of every prompt
/prefer auto_dm
     ... automatically send DM when jobs complete
/prefer variability
     ... toggle variability mode
More Commands:
/describe
/blend
/shorten
/stealth & /public    (=toggle stealth mode)
/fast & /relax        (=toggle fast mode)
/info                 (=show account info & queued jobs)
/settings             (=change bot settings)
/subscribe            (=change subscription plan)
```
---

[Writing on GitHub](https://docs.github.com/en/get-started/writing-on-github "Markdown Guide")
