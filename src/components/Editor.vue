<script setup lang="ts">
import * as Y from "yjs"
import {EditorContent, useEditor} from "@tiptap/vue-3"
import StarterKit from "@tiptap/starter-kit"
import {Collaboration} from "@tiptap/extension-collaboration";
import {WebrtcProvider} from "y-webrtc"
import {CollaborationCursor} from "@tiptap/extension-collaboration-cursor";

const ydoc = new Y.Doc();
const provider = new WebrtcProvider("tiptap-test", ydoc);
const editor = useEditor({
  content: `
    <h2>
      Hello World!
    </h2>
  `,
  extensions: [
    StarterKit,
    Collaboration.configure({
      document: ydoc,
    }),
    CollaborationCursor.configure({
      provider: provider,
      user: {
        name: `User ${Math.floor(Math.random() * 100)}`,
        color: `#${Math.floor(Math.random() * 16777215).toString(16)}`
      }
    }),
  ],
})

</script>

<template>
  <EditorContent :editor="editor" />
</template>
