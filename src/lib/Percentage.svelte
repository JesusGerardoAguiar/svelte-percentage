<script>
    // @ts-nocheck
    
      export let percent = 100;
      export let title = "Percent";
      export let lineStrokeColor = "#F2E4D0";
      export let width = 80;
      export let height = 80;
      export let graphStrokeColor = "#1B4A74";
      export let titleStyle = "";
    </script>
    
    <svg
      class="circle-chart"
      viewbox="0 0 36 36"
      width="{width}"
      height="{height}"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        class="circle-bg"
        stroke="{lineStrokeColor}"
        stroke-width={2 * 0.5}
        fill="none"
        d="M18 2.0845
                      a 15.9155 15.9155 0 0 1 0 31.831
                      a 15.9155 15.9155 0 0 1 0 -31.831"
      />
      <path
        class="circle"
        stroke="{graphStrokeColor}"
        stroke-width={2}
        stroke-dasharray="{percent},100"
        stroke-linecap="round"
        fill="none"
        d="M18 2.0845
                      a 15.9155 15.9155 0 0 1 0 31.831
                      a 15.9155 15.9155 0 0 1 0 -31.831"
      />
      <text
        class="info text-third"
        x="50%"
        y="50%"
        alignment-baseline="central"
        text-anchor="middle"
        font-size="8">{percent}%</text
      >
    </svg>
    <p class="{titleStyle}">{title}</p>
    
    <style>
      .circle-chart {
      display: block;
      margin: 10px auto;
      max-width: 100%;
    }
    
    .circle-bg {
      fill: none;
    }
    
    .circle {
      stroke-linecap: round;
      transition: stroke-dashoffset 0.5s ease 0s;
      transform: rotate(-90deg);
      transform-origin: 50% 50%;
    }
    
    .info {
      fill: #333;
    }
    </style>