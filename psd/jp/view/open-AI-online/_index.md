---
title: AI ファイルをオンラインで開く
weight: 7730
limit: 
description: AI ファイルをオンラインで開く
keywords: [open ai, open illustrator file, open AI file online, open adobe illustrator, preview of ai file, ai format open]
url: view/open-AI-online/
---

{{< blocks/products/pf/main-wrap-class >}}


{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/feature-page-section h2="AI ファイルをオンラインで開く" >}}
<p>AIフォーマットをオンラインで開くときに編集機能が必要ない場合は、このAIビューアーがさまざまな目的に適したソリューションです。Web サーバーにアップロードした後、AI ファイルをオンラインで開くことができます。AI Format はベクター形式なので、ラスタライズ処理は指定された画像サイズで行われます。追加機能については、 <a href="/psd/net">.Net</a> または <a href="/psd/java">Java</a> 必要なサイズのAIファイルを開くためのハイコードAPI</p>
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
"イラストレーターなしで AI ファイルを開く" "https://products.aspose.com/psd/view/" 
"GIST AIファイルを開くための例" "https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-ai-aitopng-aitopng-cs" 
"AIをオンラインで開くローコードアプリ" "https://products.aspose.app/psd/viewer/ai" >}}
<p>Aspose.PSD またはその他の Aspose 製品で AI ファイルを開きます。AI ファイルプレビューをオンラインでレンダリングします。</p>
{{< /blocks/products/pf/feature-page-section >}}
{{< /blocks/products/pf/main-container >}}


{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
