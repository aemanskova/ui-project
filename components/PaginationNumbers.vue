<template>
  <div class="pagination">
    <svg
      width="22"
      height="22"
      viewBox="0 0 22 22"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <rect
        x="-0.4"
        y="0.4"
        width="21.2"
        height="21.2"
        rx="10.6"
        transform="matrix(-1 0 0 1 21.2 0)"
        stroke="var(--main-text)"
        stroke-width="0.8"
      />
      <g clip-path="url(#clip0_1483_1024)">
        <path
          d="M8.53144 11.4L10.9598 13.8284L10.3942 14.394L7.00024 11L7.28304 10.7172L10.3942 7.60604L10.9598 8.17164L8.53144 10.6H15.0002V11.4H8.53144Z"
          fill="var(--main-text)"
        />
      </g>
      <defs>
        <clipPath id="clip0_1483_1024">
          <rect
            width="8"
            height="8"
            fill="var(--main-text)"
            transform="matrix(0 -1 1 0 7.00024 15)"
          />
        </clipPath>
      </defs>
    </svg>
    <a class="pagination__numbers"
      >1 2 3 4 5 <ColorText textColor="var(--yellow)">6</ColorText> ... 23</a
    >
    <svg
      width="22"
      height="22"
      viewBox="0 0 22 22"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <rect
        x="0.4"
        y="0.4"
        width="21.2"
        height="21.2"
        rx="10.6"
        stroke="var(--main-text)"
        stroke-width="0.8"
      />
      <g clip-path="url(#clip0_1483_1032)">
        <path
          d="M13.4686 11.4L11.0402 13.8284L11.6058 14.394L14.9998 11L14.717 10.7172L11.6058 7.60604L11.0402 8.17164L13.4686 10.6H6.99976V11.4H13.4686Z"
          fill="var(--main-text)"
        />
      </g>
      <defs>
        <clipPath id="clip0_1483_1032">
          <rect
            width="8"
            height="8"
            fill="var(--main-text)"
            transform="matrix(0 -1 -1 0 14.9998 15)"
          />
        </clipPath>
      </defs>
    </svg>
  </div>
</template>
<style lang="scss" scoped>
span,
a {
  margin: 0;
  padding: 0;
  color: var(--main-text);
}
.pagination {
  display: flex;
  align-items: center;
  gap: 20px;
}
</style>