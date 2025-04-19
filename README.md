# Hello GitHub!

**asdasdasd**

```javascript
"use client";
import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs";
import React, { useState } from "react";
import ReactMarkdown from "react-markdown";
import remarkGfm from "remark-gfm";

function Page() {
    const [markdown, setMarkdown] = useState("");

    const handleChange = (event) => {
        setMarkdown(event.target.value);
    };

    return (
        <div className="flex justify-center p-5">
            <Tabs defaultValue="editor">
                <TabsList>
                    <TabsTrigger value="editor">Editor</TabsTrigger>
                    <TabsTrigger value="preview">Preview</TabsTrigger>
                </TabsList>
                <TabsContent value="editor">
                    <textarea
                        value={markdown}
                        onChange={handleChange}
                        placeholder="Write your markdown here"
                        style={{
                            width: "100%",
                            height: "300px",
                            padding: "10px",
                            fontFamily: "monospace",
                            border: "1px solid #ccc",
                            borderRadius: "8px",
                            marginBottom: "20px",
                        }}
                    />
                </TabsContent>
                <TabsContent value="preview">
                    <div
                        style={{
                            maxWidth: "800px",
                            margin: "0 auto",
                            fontFamily: "Arial, sans-serif",
                            lineHeight: "1.6",
                        }}
                    >
                        <ReactMarkdown
                            children={markdown}
                            remarkPlugins={[remarkGfm]}
                        />
                    </div>
                </TabsContent>
            </Tabs>
        </div>
    );
}

export default Page;

```

Welcome to my profile! 👋
