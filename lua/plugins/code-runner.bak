return {
  "CRAG666/code_runner.nvim",
  config = function()
    require('code_runner').setup {
      -- mode = "toggleterm",
      filetype = {
        java = {
          "cd $dir &&",
          "javac $fileName &&",
          "java $fileNameWithoutExt"
        },
        python = "python3 -u",
        typescript = "deno run",
        rust = {
          "cd $dir &&",
          "rustc $fileName &&",
          "./$fileNameWithoutExt"
        },
        javascript = "node $fileName",
        -- cpp="gcc $fileName -lstdc++ -o $fileNameWithoutExt && $fileNameWithoutExt"
        cpp = {
          "cd $dir &&",
          "rm -f $fileNameWithoutExt &&",
          "g++ -g $fileName -std=c++17 -o $fileNameWithoutExt &&",
          "echo -e \"\\e[1;32mOutput:\\e[1;0m\" &&",
          "./$fileNameWithoutExt"
        },
        scss = "sass $dir/$fileName $dir/$fileNameWithoutExt.css",
      },
    }
  end,
  ft = { 'cpp', 'python', 'java', 'javascript', 'rust', 'scss' },
  opts = {
      mappings = {
      -- first key is the mode
      n = {
        -- run code
        ["<leader>rr"] = { "<cmd>w<bar>RunCode<cr>", desc = "Run code" },
        ["<leader>rf"] = { "<cmd>RunFile<cr>", desc = "Run file" },
        ["<leader>rp"] = { "<cmd>RunProject<cr>", desc = "Run project" },
        ["<leader>rc"] = { "<cmd>RunClose<cr>", desc = "Close runner" },
        -- ["<leader>rd"] = { "<cmd>!c++ -g -std=c++17 <cr>", desc = "Debug current file" },
        ["<leader>r"] = { name = " Run code" },
      },
    },
  },
  -- lazy = true,
  }

