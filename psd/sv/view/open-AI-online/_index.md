---
title: Öppna AI-fil online
weight: 7730
limit: 
description: Öppna AI-fil online
keywords: [open ai, open illustrator file, open AI file online, open adobe illustrator, preview of ai file, ai format open]
url: view/open-AI-online/
---

{{< blocks/products/pf/main-wrap-class >}}


{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/feature-page-section h2="Öppna AI-fil online" >}}
<p>När du inte behöver redigeringsfunktionen när du öppnar AI-format online är denna AI Viewer en bra lösning för många ändamål. Du kan öppna AI-fil online efter uppladdningen till webbservern. AI-format är ett vektorformat, så rastreringen fortsätter i den angivna bildstorleken. För de ytterligare funktionerna kan du använda <a href="/psd/net">.Net</a> eller <a href="/psd/java">Java</a> high-code API för att öppna AI-filer i de dimensioner du behöver</p>
{{< psd/view `https://psd-api-core-rl2ajsbv.k8s.dynabic.com/` 
`	// For the new AI format please use the following code:
	async Task<bool> OpenPdfToPng(Stream pdfFileStream, string pngFileId, Size size)
	{
		pdfFileStream.Position = 0;
		try
		{
			using var pdfDocument = new Aspose.Pdf.Document(pdfFileStream);
			var page = pdfDocument.Pages[1];
			using var imageStream = new MemoryStream();
			Resolution resolution = new Resolution(300);
			PngDevice pngDevice = new PngDevice(size.Width, size.Height, resolution);
			pngDevice.Process(page, imageStream);
			imageStream.Position = 0;
			await StorageService.Upload(pngFileId, imageStream);
			imageStream.Close();
			return true;
		}
		catch (Aspose.Pdf.InvalidPdfFileFormatException)
		{
			return false;
		}
	}
	
	// For the Old AI Formats please use the Aspose.PSD high-code API
	using (AiImage image = (AiImage)Image.Load(sourceFileName))
	{
		ImageOptionsBase options = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
		image.Save(outFileName, options);
	}` 
"Öppna AI-filer utan Illustrator" "https://products.aspose.com/psd/view/" 
"GIST Exempel på att öppna AI-filer" "https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-ai-aitopng-aitopng-cs" 
"Låg kod app för att öppna AI online" "https://products.aspose.app/psd/viewer/ai" >}}
<p>Öppna AI-fil med Aspose.PSD eller andra Aspose Products. Återge AI-filförhandsgranskningen online.</p>
{{< /blocks/products/pf/feature-page-section >}}
{{< /blocks/products/pf/main-container >}}


{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
