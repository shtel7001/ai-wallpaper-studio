# AI Wallpaper Studio — Development status

## Implemented
- Responsive mobile wallpaper editor, gradients and styles
- Local photo import, cover crop, color overlays
- Phone resolution selection and PNG export
- WebGPU availability check and extended browser hardware diagnostics
- GitHub Pages deployment workflow

## Not yet implemented
- Actual text-to-image model inference in the browser
- Mobile AI model download, caching and loading progress
- Validated support on Galaxy/iPhone devices

## Browser-side AI research
Microsoft's ONNX Runtime Web SD-Turbo sample demonstrates real local inference on suitable WebGPU hardware:
https://github.com/microsoft/onnxruntime-inference-examples/tree/main/js/sd-turbo

ONNX Runtime Web WebGPU documentation:
https://onnxruntime.ai/docs/tutorials/web/ep-webgpu.html

This example is not a drop-in mobile solution. The model weights are large and GPU memory may exceed phone limits. Before integrating, confirm model license and commercial usage, mobile memory requirements, model hosting bandwidth and CORS. A public zero-cost unlimited service cannot be guaranteed.

## Deployment
GitHub Actions workflow deploys the static files when GitHub Pages Source is set to GitHub Actions. Check Actions and Pages for deployment status.

## Next implementation milestone
Select a verified compact image-generation model that can run on a target Android phone, then integrate and measure actual inference. Until then, do not claim AI image generation is working.
