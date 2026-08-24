# Raw SVG

Berikut contoh komponen HMI `raw_svg`:

```xml
<raw_svg>
  <caption>Contoh Propeller 1</caption>
  <encoded_content>
    &lt;defs&gt;
      &lt;linearGradient id=&quot;bladeGradient&quot; x1=&quot;0%&quot; y1=&quot;0%&quot; x2=&quot;100%&quot; y2=&quot;100%&quot;&gt;
        &lt;stop offset=&quot;0%&quot; stop-color=&quot;#bd93f9&quot; /&gt;
        &lt;stop offset=&quot;100%&quot; stop-color=&quot;#8be9fd&quot; /&gt;
      &lt;/linearGradient&gt;
    &lt;/defs&gt;
    &lt;g transform=&quot;translate(150 150)&quot;&gt;
      &lt;g&gt;
        &lt;path d=&quot;M0,-8 C20,-20 65,-35 75,-15 C82,0 50,12 8,8 Z&quot; fill=&quot;url(#bladeGradient)&quot; /&gt;
        &lt;path d=&quot;M0,-8 C20,-20 65,-35 75,-15 C82,0 50,12 8,8 Z&quot; fill=&quot;url(#bladeGradient)&quot; transform=&quot;rotate(120)&quot; /&gt;
        &lt;path d=&quot;M0,-8 C20,-20 65,-35 75,-15 C82,0 50,12 8,8 Z&quot; fill=&quot;url(#bladeGradient)&quot; transform=&quot;rotate(240)&quot; /&gt;
        &lt;animateTransform attributeName=&quot;transform&quot; type=&quot;rotate&quot; from=&quot;0&quot; to=&quot;360&quot; dur=&quot;2s&quot; repeatCount=&quot;indefinite&quot; /&gt;
      &lt;/g&gt;
      &lt;circle cx=&quot;0&quot; cy=&quot;0&quot; r=&quot;10&quot; fill=&quot;#8be9fd&quot; /&gt;
      &lt;circle cx=&quot;0&quot; cy=&quot;0&quot; r=&quot;5&quot; fill=&quot;#fff&quot; /&gt;
    &lt;/g&gt;
  </encoded_content>
</raw_svg>

<!-- atau, -->

<raw_svg>
  <caption>Contoh Propeller 2</caption>
  <encoded_content>
    <![CDATA[<defs>
      <linearGradient id="bladeGradient" x1="0%" y1="0%" x2="100%" y2="100%">
        <stop offset="0%" stop-color="#bd93f9" />
        <stop offset="100%" stop-color="#8be9fd" />
      </linearGradient>
    </defs>
    <g transform="translate(350 150)">
      <g>
        <path d="M0,-8 C20,-20 65,-35 75,-15 C82,0 50,12 8,8 Z" fill="url(#bladeGradient)" />
        <path d="M0,-8 C20,-20 65,-35 75,-15 C82,0 50,12 8,8 Z" fill="url(#bladeGradient)" transform="rotate(120)" />
        <path d="M0,-8 C20,-20 65,-35 75,-15 C82,0 50,12 8,8 Z" fill="url(#bladeGradient)" transform="rotate(240)" />
        <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="20s"repeatCount="indefinite" />
      </g>
      <circle cx="0" cy="0" r="10" fill="#8be9fd" />
      <circle cx="0" cy="0" r="5" fill="#fff" />
    </g>]]>
  </encoded_content>
</raw_svg>
```

#### Contoh:

https://playground.monita.co.id/?component=raw_svg

![raw_svg](https://hackmd.io/_uploads/SJzl3YSHMx.jpg)

#### Properti selengkapnya:

| Properti        | Tipe Nilai | Nilai Baku | Pilihan             | Keterangan          |
| --------------- | ---------- | ---------- | ------------------- | ------------------- |
| caption         | string     | Text       | _null_              | Keterangan komponen |
| encoded_content | string     | _null_     | _null_              | _Raw SVG_           |
| z               | enum       | 0          | 0;1;2;3;4;5;6;7;8;9 | Posisi: z-index     |
