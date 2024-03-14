# UI Development with Dear ImGui
<div align="center">
  
![](https://img.shields.io/badge/license-MIT-green?style=plastic) ![](https://img.shields.io/badge/arch-x64%20%7C%20x86-d9654f?style=plastic) ![](https://img.shields.io/badge/config-Debug%20%7C%20Release-c0c0c0?style=plastic)

</div>

## Streamlining UI Integration with SDL and Dear ImGui

To ensure smooth visual output, a careful sequence of steps must be followed. Initially, invoking the original `SDL_GL_SwapWindow` function is crucial, followed by engaging `SDL_GL_MakeCurrent` with the original context as one of its parameters. Additionally, integrating `glFlush()` at the end of your customized `SDL_GL_SwapWindow` function is vital to eliminate any lingering flickers, enhancing display coherence and fluidity.

### Understanding Dear ImGui

Dear ImGui simplifies UI development by generating vertex buffers and command lists, seamlessly integrating them into your application's rendering pipeline. It minimizes draw calls and state transitions, offering dynamic user interfaces with reduced code volume and fewer bugs compared to traditional interfaces.

A common misconception is to confuse immediate mode GUI with immediate mode rendering, but Dear ImGui optimizes draw call batches without direct GPU interaction, improving efficiency.

## Usage

- Download the project to your computer as zip
- Extract Project to Folder.
- Make Sure Visual Studio is Installed [Click here if not installed](https://visualstudio.microsoft.com/en/thank-you-downloading-visual-studio/?sku=Community&channel=Release&version=VS2022&source=VSLandingPage&passive=false&cid=2030)
- Open the solution file (.sln).
- Select **Build Solution** from the **Build** menu or press `Ctrl+Shift+B` to compile the project.
- When the build is complete, select **Start Without Debugging** from the **Debug** menu or press `Ctrl+F5` to run the project.


## Integrating the Framework

For most platforms and C++ implementations, combining `imgui_impl_xxxx` backends without alterations is feasible. This simplifies integration, and you can easily switch backends if needed.

Integrating Dear ImGui into your custom engine involves three key steps:
1. Establishing connectivity for mouse, keyboard, and gamepad inputs.
2. Uploading a single texture to your GPU or rendering engine.
3. Implementing a render function proficient in texture binding and rendering of textured triangles.

Examples within the repository illustrate these steps, making integration achievable within a couple of hours for experienced programmers. It's recommended to explore FAQs, comments, and examples for a comprehensive understanding.
<div align="center">
  

![image](https://user-images.githubusercontent.com/100489392/157216123-1d443c52-8262-4dad-96d7-4499823c1682.png)

</div>

## Contribution

1. Fork this repo.
2. Leave a Star ⭐ on this Repo.

## Legal Disclaimer

This program is intended solely for educational purposes.


## License

This project is licensed under the MIT. For more information, see the [License](LICENSE).