<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Trendline from "./Trendline.svelte";
</script>

<Meta
  title="Example/Trendline"
  component={Trendline}
  argTypes={{
    onClick: { action: "onClick" },
  }}
/>

<Template let:args>
  <Trendline {...args} on:click={args.onClick} />
</Template>

<Story
  name="Primary"
  args={{
    primary: true,
  }}
/>
